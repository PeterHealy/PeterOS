# Log

Use one dated heading per event:

`## [YYYY-MM-DD] ingest | Source Title`

`## [YYYY-MM-DD] query | Short Question`

`## [YYYY-MM-DD] lint | Scope`

`## [YYYY-MM-DD] restructure | Scope`

## [2026-04-19] restructure | Personal OS v1 scaffold

- Reworked the repository around the agreed v1 model: `inbox`, `raw`, `sources`, `knowledge`, `records`, `reference`, `research`, `ideas`, and `queries`.
- Added domain-aware sections for `health`, `company-building`, `finance`, `reading-writing`, `travel`, and `philosophy-politics`.
- Added `reading-writing/books` and `reading-writing/blogs-essays-articles` as explicit subsections.
- Added support for blood work history, versioned finance plans, recipes with macros, and high-volume idea capture.
- Moved the seed LLM wiki pages into the new `raw/misc`, `sources/misc`, and `knowledge/meta` locations.

## [2026-04-18] bootstrap | Initial LLM wiki scaffold

- Created the initial Obsidian-friendly LLM wiki structure.
- Added the maintenance schema in [[AGENTS]].
- Ingested the seed source now stored at [[sources/misc/2026-04-18 Karpathy - LLM Wiki]].
- Added the first topic page now stored at [[knowledge/meta/LLM Wiki Pattern]].
- Confirmed the active Obsidian vault path from local Obsidian config as `/Users/petercdjh/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`.
- Direct reads of the iCloud-backed vault were blocked by macOS permissions from this environment, so no live vault content was modified.
