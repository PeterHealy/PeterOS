# Personal OS LLM Wiki

Obsidian-friendly scaffold for a Karpathy-style LLM wiki adapted into a broader personal operating system.

This repository is designed to work as a standalone Obsidian vault or as a migration target for an existing vault. It keeps the original LLM wiki pattern intact:

- immutable raw sources
- LLM-maintained wiki pages
- a schema that tells the agent how to ingest, update, and file

The schema lives in [AGENTS.md](/Users/petercdjh/Code/LLM_Wiki/AGENTS.md).

## Layout

- `inbox/` is the staging layer for fast capture and unfiled outputs.
- `raw/` holds immutable source captures and attachments.
- `sources/` holds one LLM-authored summary or digest per important source.
- `knowledge/` holds evergreen understanding by domain.
- `records/` holds longitudinal and versioned state such as blood work and finance plans.
- `reference/` holds practical lookup pages such as recipes, supplements, and visas.
- `research/` holds active dossiers for messy or unresolved topics.
- `ideas/` holds high-volume build and writing idea capture.
- `queries/` holds durable answers worth filing back into the wiki.
- `overview.md` is the current top-level synthesis.
- `index.md` is the main catalog.
- `log.md` is the append-only operational history.

## Domain Model

The main domains in v1 are:

- `health`
- `company-building`
- `finance`
- `reading-writing`
- `travel`
- `philosophy-politics`
- `misc`

Inside `reading-writing`, the primary subsections are:

- `books`
- `blogs-essays-articles`

Inside `health`, practical reference material lives under `nutrition`, including recipes and supplements.

## Obsidian Integration

On 2026-04-18, Obsidian's local config at `~/Library/Application Support/obsidian/obsidian.json` showed your active vault as:

`/Users/petercdjh/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`

That confirms the vault path, but direct reads of the iCloud-backed folder were blocked by macOS permissions from this environment. So this repo is set up as a clean starting point that matches your current workflow style without mutating the live vault yet.

Practical next options:

1. Open `/Users/petercdjh/Code/LLM_Wiki` directly as a separate Obsidian vault.
2. Copy this scaffold into the existing `Notes` vault once you are happy with the workflow.
3. Grant direct access to the iCloud vault later if you want Codex to adapt the live vault in place.

## Suggested Workflow

1. Paste a source or note into `inbox/sources/`, or hand it to Codex directly in chat.
2. Ask Codex to ingest it.
3. Codex normalizes the source into `raw/` and `sources/`.
4. Codex updates the right long-term page in `knowledge/`, `records/`, `reference/`, `research/`, `ideas/`, or `queries/`.
5. Review the result in Obsidian when useful, but do not manually maintain the filing system unless you want to.
