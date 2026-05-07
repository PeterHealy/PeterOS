---
type: query
title: How Should I Read My Wiki In Obsidian?
status: active
created: 2026-05-07
updated: 2026-05-07
question: How should I as a human read my wiki on Obsidian?
answered_on: 2026-05-07
based_on:
  - "[[index]]"
  - "[[overview]]"
tags:
  - query
  - llm-wiki
  - obsidian
---

# How Should I Read My Wiki In Obsidian?

## Short Answer

Use Obsidian as a browsing, recall, and synthesis surface, not as the main maintenance interface.

Start from [[overview]] when you want orientation, [[index]] when you want navigation, and the relevant domain page when you already know what area you care about. Let Codex do most filing, summarizing, and cross-linking.

## The Reading Order

### 1. Start With The Map

Open [[overview]] first if you have not been in the vault recently.

Use it to answer:

- What is currently in the wiki?
- What domains are active?
- What has been imported but not yet fully synthesized?
- What should I try next?

Then open [[index]] when you want the full catalog.

Treat [[index]] as the master table of contents, not as a page to read linearly every time.

### 2. Read By Intent

Pick the folder based on what you are trying to do:

- `knowledge/` when you want durable understanding.
- `reference/` when you want a practical checklist, tool, protocol, recipe, or lookup page.
- `research/` when the topic is unfinished, contradictory, or still source-heavy.
- `records/` when you want historical state, dated decisions, blood work, finance versions, or other longitudinal material.
- `ideas/` when you want raw creative surface area.
- `queries/` when you want saved answers and decision memos.
- `sources/` when you want to inspect what one article, book, thread, or digest contributed.
- `raw/` only when you need provenance or the original capture.

### 3. Prefer Synthesis Over Raw Notes

Do not read `raw/` casually.

The intended path is:

1. Read the evergreen, reference, dossier, record, idea, or saved query.
2. Follow links back to `sources/` when you want evidence.
3. Follow links back to `raw/` only when you need the original highlight, capture, pasted email, or metadata.

Raw files are the source layer. They are not supposed to be pleasant human reading.

### 4. Use Backlinks As The Second Table Of Contents

When reading a useful page, open Obsidian backlinks and outgoing links.

Use outgoing links to go down the evidence chain:

- evergreen page
- source summary
- raw capture

Use backlinks to go up the synthesis chain:

- raw capture
- source summary
- evergreen page, research dossier, reference page, query, or idea

This is where the LLM wiki pattern becomes useful: pages are not just folders; they are traces of how source material became reusable judgment.

### 5. Read Different Page Types Differently

Evergreen pages are for stable models. Read them slowly and expect them to change when better sources arrive.

Research dossiers are working files. Read them as unresolved maps, not as final conclusions.

Reference pages are operational. Read them when you are about to do something.

Records are historical. Read them to understand what was true at a time.

Source summaries are evidence pages. Read them when you want the argument of a specific source without reopening the original.

Raw captures are provenance. Read them only when you need to audit the source trail.

Saved queries are reusable answers. Read them when the question itself is likely to recur.

Ideas are intentionally messy. Read them for optionality, not truth.

## Recommended Obsidian Habits

- Pin [[overview]] and [[index]].
- Add bookmarks for active domain pages like [[knowledge/company-building/README|Company Building]], [[knowledge/ai-agents/README|AI Agents]], and [[knowledge/reading-writing/README|Reading And Writing]].
- Use graph view sparingly; backlinks are usually more useful.
- Use search for nouns, not folder paths.
- When a page feels useful but underdeveloped, ask Codex to promote, merge, or normalize it.
- When you find a contradiction, ask Codex to record the disagreement rather than choosing a winner too early.

## The Best Human Loop

1. Browse from [[overview]] or a domain page.
2. Read one synthesis page.
3. Follow one or two source links if you care about the basis.
4. Capture reactions as short notes or ask Codex to ingest them.
5. Ask a synthesis question when several pages feel connected.
6. Let Codex file the answer back into the wiki.

The human job is judgment, taste, curiosity, and recall. The agent job is capture, cleanup, linking, and maintenance.

