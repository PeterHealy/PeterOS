# Log

Use one dated heading per event:

`## [YYYY-MM-DD] ingest | Source Title`

`## [YYYY-MM-DD] query | Short Question`

`## [YYYY-MM-DD] lint | Scope`

`## [YYYY-MM-DD] restructure | Scope`

## [2026-05-07] maintenance | Repo readiness review

- Reviewed [[AGENTS]], [[README]], [[raw/README]], and [[sources/README]] before the next ingestion push.
- Clarified that [[sources/README]] pages are the main Obsidian starting point and that [[raw/README]] is the provenance/replay layer rather than the normal browsing surface.
- Updated source workflow guidance so short link-plus-highlights submissions can keep full highlights and PNotes in the canonical source page, while long captures, books, PDFs, transcripts, lab records, and messy imports stay primarily in `raw/`.
- Normalized imported book source pages from `status: imported` to `status: processed` while keeping their highlights-based limits explicit.
- Added [[templates/README]] and linked it from [[index]] so page templates are discoverable.

## [2026-05-07] maintenance | Book source-page upgrade

- Updated [[AGENTS]], [[sources/README]], [[sources/reading-writing/books/README]], [[raw/reading-writing/books/README]], [[knowledge/reading-writing/books/README]], and [[templates/book-page]] so book source pages are treated as highlight-led reading pages rather than generic book summaries.
- Regenerated all 23 imported Kobo book source pages under [[sources/reading-writing/books/README]] from their raw captures in `raw/reading-writing/books/obsidian-import/`.
- Kept complete exact quote exports in the raw layer and made each source page navigable through raw block links, highlight maps, exact personal notes, capture-based synthesis, reusable ideas, possible uses, open questions, and filing notes.
- Updated [[sources/reading-writing/books/Obsidian Book Highlights Digest]] to describe the new highlight-led standard.

## [2026-05-07] maintenance | Obsidian article source-page upgrade

- Reprocessed the imported Obsidian blog, essay, and article source pages to match the higher-quality source-hub format used by [[sources/reading-writing/blogs-essays-articles/Packy McCormick and Will OBrien - The Great Blue Frontier]].
- Upgraded 19 imported URL-based pages into full-source summaries with summary basis, source summary, key ideas, exact `Your Captures`, capture-based synthesis, claims, caveats, and related links.
- Left the two X-based pages explicitly capture-based where direct X retrieval was unavailable: [[sources/reading-writing/blogs-essays-articles/The Kobeissi Letter - What If AI Doesnt Actually End The World]] and [[sources/reading-writing/blogs-essays-articles/Will Manidis - Civis Romanus Sum]].
- Updated [[sources/reading-writing/blogs-essays-articles/README]] and [[sources/reading-writing/blogs-essays-articles/Obsidian Essay And Blog Highlights Digest]] so the imported pages are no longer presented as pending stubs.
- Updated [[index]] to reflect the upgraded source-hub state.

## [2026-05-07] maintenance | Canonical source-page migration

- Updated [[AGENTS]] so `[SUBMIT]` creates one canonical human-readable source page plus a raw archive, with promotion into knowledge, reference, research, or ideas only when reusable.
- Replaced `Your Notes` guidance with `Your Captures`: exact user notes, PNotes, and imported `My thoughts` belong there; LLM interpretation belongs in separate synthesis sections.
- Created one canonical source page for each imported Obsidian book note under [[sources/reading-writing/books/README]].
- Created one canonical source page for each imported Obsidian article, essay, or web post under [[sources/reading-writing/blogs-essays-articles/README]].
- Converted the old book and article digest pages into migration indexes instead of treating each import batch as a single source.
- Normalized existing source pages so exact captures are separated from capture-based synthesis.

## [2026-05-07] ingest | Zeneca - All About Local LLMs

- Captured the user-highlighted excerpts from Zeneca's April 21, 2026 article on local LLMs, with emphasis on Mac unified memory, large-model fit, power draw, and noise.
- Stored the raw capture under [[raw/ai-agents/zeneca-all-about-local-llms-highlight-capture]].
- Added a full-source summary at [[sources/ai-agents/Zeneca - All About Local LLMs]] after confirming the canonical URL was accessible.
- Added [[knowledge/ai-agents/Local LLM Operating Model]] as an evergreen hybrid cloud/local model strategy note.
- Added [[reference/ai-agents/Local LLM Setup]] as a practical setup reference for LM Studio, Ollama, hardware choices, and local OpenAI-compatible endpoints.
- Updated [[reference/Tools And Websites]] with local-LLM tools and model infrastructure mentioned by the source.

## [2026-05-07] query | When Are Pages Created Outside Raw?

- Answered when and why the wiki should create pages outside the immutable `raw/` layer.
- Filed the saved answer at [[queries/When Are Pages Created Outside Raw]].
- Linked the query from [[index]].

## [2026-05-07] query | How Should I Read My Wiki In Obsidian?

- Answered the operating question of how a human should browse and read this LLM wiki in Obsidian.
- Filed the saved answer at [[queries/How Should I Read My Wiki In Obsidian]].
- Linked the query from [[index]].

## [2026-05-07] query | Wiki Recall System

- Added [[ideas/build/Wiki Recall System]] as a build-spec note for turning ingested wiki material into active recall questions with answer reveal and spaced resurfacing.
- Updated [[ideas/build/README]] and [[index]] so the idea is findable.
- Added reusable tool references for Anki, Telegram Bot API, Discord Webhooks, Apple WidgetKit, and Android App Widgets to [[reference/Tools And Websites]].
- Design emphasis: keep scheduling and card storage separate from delivery surfaces so email, Telegram, Discord, web UI, and lockscreen widgets can share the same recall engine.
- Repository decision: build the product code in a separate `wiki-recall` repo that references `LLM_Wiki` as its data source, with any writeback limited to an explicit recall records area.

## [2026-05-07] ingest | Packy McCormick and Will O'Brien - The Great Blue Frontier

- Captured the user-provided highlights and PNotes from the Not Boring essay on the ocean as a frontier market.
- Stored the raw capture under [[raw/reading-writing/blogs-essays-articles/not-boring-the-great-blue-frontier-highlight-email]].
- Added a full-source summary at [[sources/reading-writing/blogs-essays-articles/Packy McCormick and Will OBrien - The Great Blue Frontier]] after reading the accessible canonical URL.
- Added [[knowledge/company-building/Frontier Cost Collapse]] as a reusable model for access breakthroughs, multiplicative technology curves, and latent demand.
- Updated [[reference/Tools And Websites]] with reusable ocean infrastructure companies and platforms mentioned in the source.

## [2026-05-07] ingest | Dom Cooke - Beyond the Sky

- Captured the user's highlighted excerpts and PNotes from Colossus's profile of Jeffrey Yan and Hyperliquid under [[raw/company-building/execution/dom-cooke-beyond-the-sky-jeffrey-yan-hyperliquid-highlight-capture]].
- Read the accessible canonical article and added a full-source summary at [[sources/company-building/execution/Dom Cooke - Beyond the Sky]].
- Updated [[research/company-building/Mission-Driven Work Intensity]] with the Hyperliquid/Yan case: trained work capacity, high-talent peer environments, and directionally confident execution under uncertainty.
- Added reusable site entries for Colossus and Hyperliquid to [[reference/Tools And Websites]].
- User-note emphasis: "beyond the sky" should calibrate toward the next reachable level rather than diminish results; peer group and grind are central to raising the ceiling.

## [2026-05-07] ingest | Robin Hanson - My Class And Goals

- Captured the user-submitted Overcoming Bias URL and personal note about using the funeral question to find meaning in daily life.
- Stored the raw submitted capture under [[raw/reading-writing/blogs-essays-articles/robin-hanson-my-class-and-goals-submit]].
- Added a full-source summary at [[sources/reading-writing/blogs-essays-articles/Robin Hanson - My Class And Goals]].
- Added [[knowledge/philosophy-politics/Stated Life Goals And The Funeral Test]] as an evergreen note on writing explicit life-goal essays and judging days against chosen aims.
- Source access note: the canonical article was accessible directly on 2026-05-07.

## [2026-05-07] ingest | Packy McCormick and Pim De Witte - World Models

- Captured the user's submitted excerpts from Not Boring's March 19, 2026 essay on world models under [[raw/ai-agents/not-boring-world-models-highlight-capture]].
- Read the accessible canonical article and added a full-source summary at [[sources/ai-agents/Packy McCormick and Pim De Witte - World Models Computing the Uncomputable]].
- Added [[knowledge/ai-agents/README]] and [[knowledge/ai-agents/World Models]] as the first evergreen pages in the AI-agent knowledge domain.
- Updated [[reference/Tools And Websites]] with reusable AI-agent and robotics resources from the source.
- User-note emphasis: world models depend on latent action-conditioned prediction, explicit uncertainty over possible futures, actions as behavioral compression, and games as unusually clean action-outcome datasets.

## [2026-05-07] ingest | Scott Alexander - Half A Month Of Consolation Writing Advice

- Captured the user-selected excerpts from Scott Alexander's April 21, 2026 Astral Codex Ten article on writing advice.
- Stored the raw highlight capture under [[raw/reading-writing/blogs-essays-articles/scott-alexander-half-a-month-of-consolation-writing-advice-highlight-email]].
- Added a full-source summary at [[sources/reading-writing/blogs-essays-articles/Scott Alexander - Half A Month Of Consolation Writing Advice]].
- Added [[knowledge/reading-writing/blogs-essays-articles/Nonfiction Writing Discipline]] as an evergreen page for reusable nonfiction writing heuristics.
- Source access note: the canonical article URL was accessible during ingest, so the source summary is based on the full article plus the user's selected excerpts.

## [2026-05-07] restructure | [SUBMIT] Ingest Trigger

- Updated [[AGENTS]] so future user messages beginning with `[SUBMIT]` are treated as source material to ingest into the LLM wiki.
- Defined the trigger as the full ingest workflow: preserve the raw source, create or update a source summary, promote durable insights, update [[index]], and append [[log]].
- Updated [[index]] to reflect the new message trigger in the schema summary.

## [2026-05-06] ingest | Nate Martins - Reluctantly Influential

- Captured the user's highlighted excerpt and attached-image transcription from the First Round Review profile of Lenny Rachitsky under [[raw/company-building/execution/lenny-rachitsky-sprint-board-highlight]].
- Read the canonical article and added a full-source summary at [[sources/company-building/execution/Nate Martins - Reluctantly Influential]].
- Added [[reference/company-building/execution/Self-Imposed Accountability Board]] as a reusable execution playbook for biweekly goals, midpoint updates, and sprint reviews.
- Updated [[reference/Tools And Websites]] with reusable tool and website mentions from the source.
- User-note emphasis: accountability can come from visibly committing goals to trusted people even when they have no responsibility to respond.

## [2026-05-06] restructure | Human-Readable Page Naming

- Updated [[AGENTS]] so new source, raw, and query pages default to human-readable filenames instead of date-prefixed filenames.
- Dates should live in frontmatter fields such as `captured`, `published`, `ingested`, `created`, `updated`, and `recorded_on`.
- Renamed existing date-prefixed source, raw, digest, record, and idea markdown pages to human-readable filenames, updating path-based wikilinks across the vault.
- Added missing `captured` metadata to raw markdown captures and confirmed source summaries carry `published` and `ingested` fields.
- Renamed the Alex Lieberman PNG attachment to remove its date prefix and updated the embed link.

## [2026-05-06] ingest | Robin Hanson - The Great Filter

- Captured the user's pasted highlights and PNotes from Robin Hanson's Great Filter essay under [[raw/reading-writing/blogs-essays-articles/robin-hanson-great-filter-highlight-email]].
- Read the full source URL and added a full-source summary at [[sources/reading-writing/blogs-essays-articles/Robin Hanson - The Great Filter]].
- Added [[knowledge/philosophy-politics/The Great Filter]] as an evergreen page on the Great Filter, Fermi silence, evidence direction, and future-risk implications.
- User-note emphasis: alternative routes to cosmic expansion increase the filter burden; secret-alien explanations must also account for the absence of visible competitive resource use.

## [2026-05-06] restructure | URL Article Highlight Ingest Rules

- Updated [[AGENTS]] so URL-based article, essay, and blog ingests summarize the canonical source when accessible, not just the user's pasted highlights.
- Clarified that `raw/` preserves the user-provided email, snippets, separators, and PNotes as the immutable capture.
- Updated the source-summary template and folder READMEs to include summary-basis tracking and a separate `Your Notes` section.
- Added the fallback rule that inaccessible sources must be marked as excerpt-based or metadata-based rather than treated as full-source summaries.

## [2026-05-05] ingest | Obsidian Notes Import

- Imported 50 markdown notes from `/Users/petercdjh/obsidian/notes` into the raw layer while preserving the original book highlights, web highlights, and personal annotations.
- Stored book-highlight captures under `raw/reading-writing/books/obsidian-import/` and web-highlight captures under `raw/reading-writing/blogs-essays-articles/obsidian-import/`.
- Stored personal and miscellaneous captures under `raw/personal/obsidian-import/`.
- Added [[records/Obsidian Notes Import Manifest]] as the import map.
- Added source digests at [[sources/reading-writing/books/Obsidian Book Highlights Digest]] and [[sources/reading-writing/blogs-essays-articles/Obsidian Essay And Blog Highlights Digest]].
- Extracted personal build ideas into [[ideas/build/Imported Build Ideas From Obsidian]] and skill notes into [[reference/personal/Skills To Improve]].
- Added reusable tools and learning sites from the personal notes to [[reference/Tools And Websites]].

## [2026-04-27] ingest | Alex Lieberman - Claude Code Replaced My 20-Person Marketing Team

- Captured the user's notes from an Alex Lieberman video about GTM engineering, templated ad creation, landing-page iteration, and the analytics bottleneck.
- Stored the raw source under [[raw/company-building/marketing/alex-lieberman-claude-code-replaced-my-20-person-marketing-team]] and copied the related ad-generator screenshot into `raw/`.
- Added a source summary at [[sources/company-building/marketing/Alex Lieberman - Claude Code Replaced My 20-Person Marketing Team]].
- Added a reusable workflow page at [[reference/company-building/marketing/AI-Assisted GTM Testing Loop]].
- Verification note: kept `published` blank because the video's publish date was not confirmed during this ingest.
- Caveat note: the source suggests using Google's Indexing API for landing-page indexing, but the summary records Google's official restriction that the API is only for job posting and livestream pages.

## [2026-04-27] restructure | Tools And Websites Registry

- Added [[reference/Tools And Websites]] as the canonical place to store reusable tool and website mentions with URLs and one-line descriptions.
- Updated [[AGENTS]] so future source ingests extract concrete tool and website mentions into the shared registry.
- Updated [[reference/README]] and [[index]] so the new registry is easy to find from normal repo navigation.

## [2026-04-27] ingest | Om Patel - First 100 Paying Users With Zero Ad Spend

- Captured the full user-provided text of a March 13, 2026 X post about early customer acquisition without paid ads.
- Stored the raw source under [[raw/company-building/marketing/om-patel-first-100-paying-users-zero-ad-spend]].
- Added a source summary at [[sources/company-building/marketing/Om Patel - First 100 Paying Users With Zero Ad Spend]].
- Added a reusable marketing reference page at [[reference/company-building/marketing/First 100 Users Without Paid Ads]].
- Source access note: the local capture relies on the title and body text provided directly by the user; the published date was derived from the X status ID.

## [2026-04-27] ingest | natiakourdadze - How Id Promote My Startup If I Had 0 Followers

- Captured the full user-provided text of a March 11, 2026 X post about startup promotion through competitor mention monitoring, community seeding, and borrowed audiences.
- Stored the raw source under [[raw/company-building/marketing/natiakourdadze-how-id-promote-my-startup-if-i-had-0-followers]].
- Added a source summary at [[sources/company-building/marketing/natiakourdadze - How Id Promote My Startup If I Had 0 Followers]].
- Added a reusable marketing reference page at [[reference/company-building/marketing/Startup Promotion Without an Audience]].
- Source access note: direct X retrieval was unreliable, so the local capture relies on the title and body text provided directly by the user; the published date was derived from the X status ID.

## [2026-04-27] ingest | Sahil Lavingia - Minimalist Entrepreneur Skills

- Captured `slavingia/skills` as an external agent skill library with company-building content.
- Stored a raw metadata stub at [[raw/ai-agents/slavingia-skills]].
- Added a source summary at [[sources/ai-agents/Sahil Lavingia - Minimalist Entrepreneur Skills]].
- Added a reusable reference page at [[reference/ai-agents/skills/Minimalist Entrepreneur Skills]].
- Decision note: kept it as a reference rather than vendoring the Claude plugin into the wiki.

## [2026-04-27] ingest | natiakourdadze - How To Build a Personal Brand on X in 2026

- Captured the full user-provided text of a March 10, 2026 X post about personal-brand growth, algorithm heuristics, and viral hooks.
- Stored the raw source under [[raw/company-building/marketing/natiakourdadze-how-to-build-a-personal-brand-on-x-in-2026]].
- Added a source summary at [[sources/company-building/marketing/natiakourdadze - How To Build a Personal Brand on X in 2026]].
- Added a reusable marketing reference page at [[reference/company-building/marketing/X Personal Brand Growth Tactics]].
- Source access note: direct X retrieval was unreliable, so the local capture relies on the title and body text provided directly by the user; the published date was derived from the X status ID.

## [2026-04-27] ingest | Greg Isenberg - Agent-First Startups Tweet

- Replaced the previously partial local capture with the full post text provided directly in chat.
- Expanded [[sources/company-building/ai/Greg Isenberg - Agent-First Startups Tweet]] to include the pricing, services-compression, founder-selection, and distribution claims.
- Updated [[research/company-building/Agent-First Startups]] with a clearer agent-native GTM model and its main contradictions.
- Added [[knowledge/company-building/Agent-Native Go-To-Market]] as a reusable heuristic page for evaluating vertical AI opportunities.
- Source access note: direct X retrieval remained truncated, so the canonical local capture now relies on the user-provided full text.

## [2026-04-27] ingest | Boz - A Career Cold Start Algorithm

- Captured Boz's March 8, 2018 article on ramping into a new team or project by running recursive listening interviews.
- Stored the raw source capture under [[raw/company-building/execution/boz-career-cold-start-algorithm]].
- Added a source summary at [[sources/company-building/execution/Boz - A Career Cold Start Algorithm]].
- Added [[reference/company-building/execution/README]] as an explicit home for reusable execution playbooks.
- Added a reusable reference page at [[reference/company-building/execution/Career Cold Start Algorithm]].

## [2026-04-27] ingest | chameleon_jeff - Hard Work Over Smart Work Thread

- Captured the user-pasted full text of @chameleon_jeff's March 4, 2023 X thread about hard work, focus, and mission-driven execution.
- Stored the raw thread capture under [[raw/company-building/execution/chameleon-jeff-hard-work-over-smart-work-thread]].
- Added a source summary at [[sources/company-building/execution/chameleon_jeff - Hard Work Over Smart Work Thread]].
- Opened a working dossier at [[research/company-building/Mission-Driven Work Intensity]].
- Source access note: the thread was provided directly in chat and preserved as a single continuous capture because the tweets all expressed one idea.

## [2026-04-19] ingest | ETHSkills

- Captured `ethskills.com` as an AI-agent skill library reference.
- Stored a raw metadata stub at [[raw/ai-agents/ethskills]].
- Added a source summary at [[sources/ai-agents/ETHSkills]].
- Added [[reference/ai-agents/README]] and [[reference/ai-agents/skills/README]] as a dedicated home for external skill resources.
- Added a reusable reference page at [[reference/ai-agents/skills/ETHSkills]].

## [2026-04-19] ingest | Ben Alistor - Content Rules LinkedIn Post

- Captured Ben Alistor's LinkedIn post about three filters for stronger content.
- Stored the accessible raw excerpt at [[raw/company-building/marketing/ben-alistor-content-rules-linkedin-post]].
- Added a source summary at [[sources/company-building/marketing/Ben Alistor - Content Rules LinkedIn Post]].
- Added a reusable reference page at [[reference/company-building/marketing/Ben Alistor Content Rules]].
- Source access note: direct LinkedIn page fetch was unreliable, so the raw capture preserves the accessible post text from search results and marks the capture as partial.

## [2026-04-19] ingest | Bryan Johnson - Protocol

- Captured Bryan Johnson's public protocol site as a non-personal health reference.
- Stored a raw metadata stub at [[raw/health/bryan-johnson-protocol]] because the canonical source is a live website.
- Added a source summary at [[sources/health/Bryan Johnson - Protocol]].
- Added a canonical reference page at [[reference/health/protocols/Bryan Johnson Protocol]].
- Added `reference/health/` and `reference/health/protocols/` as explicit homes for high-quality external health guides that are worth revisiting.

## [2026-04-19] ingest | Greg Isenberg - Agent-First Startups Tweet

- Captured Greg Isenberg's X post from April 18, 2026 about agent-first startups.
- Stored the accessible raw excerpt under [[raw/company-building/ai/greg-isenberg-agent-first-startups-tweet]].
- Added a source summary at [[sources/company-building/ai/Greg Isenberg - Agent-First Startups Tweet]].
- Opened a working dossier at [[research/company-building/Agent-First Startups]].
- Source access note: direct X page retrieval was truncated, so the raw capture preserves the accessible embed/snippet text and marks the capture as partial.

## [2026-04-19] restructure | Personal OS v1 scaffold

- Reworked the repository around the agreed v1 model: `inbox`, `raw`, `sources`, `knowledge`, `records`, `reference`, `research`, `ideas`, and `queries`.
- Added domain-aware sections for `health`, `company-building`, `finance`, `reading-writing`, `travel`, and `philosophy-politics`.
- Added `reading-writing/books` and `reading-writing/blogs-essays-articles` as explicit subsections.
- Added support for blood work history, versioned finance plans, recipes with macros, and high-volume idea capture.
- Moved the seed LLM wiki pages into the new `raw/misc`, `sources/misc`, and `knowledge/meta` locations.

## [2026-04-18] bootstrap | Initial LLM wiki scaffold

- Created the initial Obsidian-friendly LLM wiki structure.
- Added the maintenance schema in [[AGENTS]].
- Ingested the seed source now stored at [[sources/misc/Karpathy - LLM Wiki]].
- Added the first topic page now stored at [[knowledge/meta/LLM Wiki Pattern]].
- Confirmed the active Obsidian vault path from local Obsidian config as `/Users/petercdjh/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`.
- Direct reads of the iCloud-backed vault were blocked by macOS permissions from this environment, so no live vault content was modified.
