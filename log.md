# Log

Use one dated heading per event:

`## [YYYY-MM-DD] ingest | Source Title`

`## [YYYY-MM-DD] query | Short Question`

`## [YYYY-MM-DD] lint | Scope`

`## [YYYY-MM-DD] restructure | Scope`

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
