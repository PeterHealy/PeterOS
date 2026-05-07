---
type: idea
title: Wiki Recall System
status: active
created: 2026-05-07
updated: 2026-05-07
tags:
  - build-idea
  - reading-writing
  - recall
  - memory
  - personal-os
source_pages:
  - "[[knowledge/meta/LLM Wiki Pattern]]"
  - "[[ideas/build/Imported Build Ideas From Obsidian]]"
---

# Wiki Recall System

## Core Idea

Build a recall layer on top of the LLM wiki so important ideas from ingested material are not merely filed, but periodically retrieved from memory.

The system should prefer repetitive recall over repetitive reading:

- Turn selected source summaries, evergreen notes, and personal notes into short recall questions.
- Show the question first.
- Require an attempted answer before revealing the actual answer.
- Recall new material several times in the first week.
- After the first week, resurface it sporadically so useful ideas stay alive.

## Why It Fits This Wiki

The current [[knowledge/meta/LLM Wiki Pattern]] already separates raw capture, source summaries, durable knowledge, and references. A recall system can use the maintained synthesis layer rather than trying to review entire raw captures.

This also connects to the imported build ideas around:

- essay review and recommendation
- chess puzzle review through spaced re-solving

Those are narrower examples of the same pattern: important material should come back as a challenge, not just sit in an archive.

## Recommended MVP

Start as a local wiki-backed system before building a full app.

MVP behavior:

- Store recall cards as Markdown or JSON under `records/recall/`.
- Generate cards when a source summary or evergreen page is created or materially updated.
- Create a daily due list containing 3-10 cards.
- Deliver through one low-friction channel first.
- Log each response as `forgot`, `partial`, or `remembered`.
- Reveal the answer only after the user attempts recall.

The first delivery surface should be whichever one is easiest to actually see daily:

- Telegram bot: good for personal mobile prompts and inline answer buttons.
- Email: lowest infrastructure complexity and good for slower reflective recall.
- Discord webhook: easy if there is already a personal Discord workspace.
- Local web app: best once review history, filtering, and card editing matter.

## Recall Card Shape

Each card should be small enough to answer without rereading the source.

Fields:

- `id`
- `source_page`
- `question`
- `answer`
- `why_it_matters`
- `tags`
- `created`
- `due_at`
- `last_reviewed`
- `interval_days`
- `ease`
- `lapses`
- `status`

Example:

```markdown
Q: In the LLM wiki pattern, why keep raw captures separate from source summaries?

A: Raw captures preserve the original material, while source summaries are the maintained interpretation layer. Separating them keeps the source traceable without turning the wiki into a dump of excerpts.
```

## Scheduling Rule

Use a simple schedule first:

- New card: same day or next morning.
- If remembered: +1 day, +3 days, +7 days, +21 days, +45 days, +90 days.
- If partial: repeat tomorrow and keep the interval short.
- If forgotten: show the answer, ask again later the same day or next day, then restart the early schedule.

This is enough for a personal system. A mature version could adopt an Anki-like scheduler, but the first implementation should optimize for generating good questions and making review frictionless.

## Question Generation Rules

Good questions should ask for compressed understanding, not trivia.

Prefer:

- "What is the core argument?"
- "What distinction matters here?"
- "What would this imply in practice?"
- "What would I do differently if I remembered this?"
- "Which source introduced this idea?"

Avoid:

- exact wording tests
- date trivia unless dates are central
- overly broad prompts like "Summarize this article"
- cards that require rereading a whole page to answer

## Review Experience

The interaction should be:

1. Show one question.
2. User answers mentally or writes a short answer.
3. User taps or types "show answer".
4. System reveals the answer and source page link.
5. User marks recall quality.
6. Scheduler updates the next due date.

For a message-based version, the answer can be hidden behind a second message or button. For a web app, the card can have a reveal state and keyboard shortcuts.

## Architecture

Local-first architecture:

- Extractor: reads changed pages from `sources/`, `knowledge/`, and selected `ideas/`.
- Card generator: asks an LLM to propose recall cards from the maintained wiki layer.
- Card store: Markdown or SQLite.
- Scheduler: selects due cards.
- Delivery adapter: Telegram, email, Discord, or local web UI.
- Review logger: records recall quality and next due date.

Keep delivery separate from scheduling. That allows the same card engine to power email now, Telegram later, and phone lock screen widgets eventually.

## Repository Boundary

Build the recall system in a separate repo that references this wiki as a data source.

Recommended split:

- `LLM_Wiki`: source of truth for raw captures, source summaries, evergreen notes, references, ideas, and recall design notes.
- `wiki-recall`: product code for card generation, scheduling, delivery adapters, review logging, and any web or mobile UI.

The recall repo should treat the wiki path as configuration, for example `LLM_WIKI_PATH=/Users/petercdjh/Code/LLM_Wiki`. It should read from the maintained wiki layer and write back only to a narrow, agreed location such as `records/recall/` or an export file.

Reasons to keep it separate:

- The wiki remains a clean Obsidian-first knowledge base rather than becoming an app monorepo.
- App dependencies, secrets, bot tokens, build artifacts, mobile code, and deployment config stay out of the knowledge repo.
- The recall engine can eventually be reused with another vault or shipped independently.
- Versioning product code separately makes experimentation easier without polluting the wiki history.

Exception: the first prototype can live as a small script inside `LLM_Wiki/scripts/` if the only goal is to prove card extraction against local Markdown. Move it to a separate repo once it needs dependencies, a scheduler, a bot token, database state, or a UI.

## Long-Term Lockscreen Version

The lockscreen version should be treated as a later display surface, not the core system.

For iPhone, the natural route is a WidgetKit widget that shows one due question and deep-links into the app or web view to reveal the answer. Apple documents WidgetKit support for Lock Screen widgets and Live Activities.

For Android, the natural route is an app widget backed by the same due-card API. Android widget support depends on the widget host and lockscreen surface, so this should come after the core scheduler works.

## Open Questions

- Should generated cards be auto-accepted, or staged for review before entering the schedule?
- Should recall happen only for personally marked important ideas, or all ingested source summaries?
- Should answers be written by the user and stored, or is mental recall plus a rating enough?
- Should the system send one daily bundle or interrupt with individual questions?
- Should cards belong to source pages, evergreen pages, or both?

## Suggested Next Step

Build the smallest version:

- Generate cards from one source summary.
- Store them locally in `records/recall/cards.json`.
- Create a command that prints today's due card.
- Add a reveal step and a recall rating.
- Only after that works, wire it to Telegram, email, or Discord.

## Related Pages

- [[knowledge/meta/LLM Wiki Pattern]]
- [[ideas/build/Imported Build Ideas From Obsidian]]
- [[reference/Tools And Websites]]

## External References

- [Anki Manual: Background](https://docs.ankiweb.net/background.html)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Discord Webhook Resource](https://docs.discord.com/developers/resources/webhook)
- [Apple WidgetKit](https://developer.apple.com/documentation/WidgetKit/)
- [Android App Widgets](https://developer.android.com/develop/ui/views/appwidgets)
