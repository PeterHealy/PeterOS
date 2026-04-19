# AGENTS.md

This repository is a Personal OS built on the LLM wiki pattern. Treat it as a maintained knowledge base, not a chat scratchpad.

## Core Model

The repository has three layers:

- `raw/` is the immutable source layer.
- the rest of the wiki is the LLM-maintained interpretation and synthesis layer.
- this file is the schema layer that tells the agent how to maintain the system.

The user should be able to mostly use Codex for ingestion, filing, and upkeep while Obsidian remains the browsing interface.

## Repository Model

- `inbox/sources/` is the staging area for fast unstructured intake.
- `inbox/outputs/` is the staging area for useful answers that should be filed later if they are not yet normalized.
- `raw/` stores immutable source captures such as tweets, podcast snippets, Kobo highlights, PDFs, spreadsheets, lab results, and article excerpts.
- `sources/` stores one summary or digest page per important source or source bundle.
- `knowledge/` stores evergreen pages by domain.
- `records/` stores longitudinal or versioned material such as blood work history and finance strategy versions.
- `reference/` stores practical lookup pages such as recipes, supplements, and visa notes.
- `research/` stores active dossiers for unfinished or messy topics.
- `ideas/` stores high-volume idea capture.
- `queries/` stores durable answers, memos, and analyses that came out of asking questions.
- `index.md` is the main catalog and should be updated whenever pages are created, renamed, promoted, or materially changed.
- `log.md` is append-only and should be updated for each ingest, major query, restructure, or lint pass.
- `overview.md` is the top-level synthesis of the repository.

## Active Domains

The default v1 domains are:

- `health`
- `company-building`
- `finance`
- `reading-writing`
- `travel`
- `philosophy-politics`
- `misc`

Within `reading-writing`, keep separate subsections for:

- `books`
- `blogs-essays-articles`

Within `health`, treat `nutrition` as the home for recipes and supplements.

## Page Types

Use these page types deliberately:

- `raw-source`: immutable source capture
- `source-summary`: one-source or digest synthesis
- `evergreen`: cleaned-up durable knowledge
- `research-dossier`: active working file with unresolved material
- `record`: dated or longitudinal tracked state
- `reference`: practical lookup material
- `idea`: fast capture with minimal friction
- `query`: durable saved answer or memo
- `overview`: top-level repo synthesis

## Default Workflow

1. Start by reading `index.md`, then follow links into the relevant pages.
2. For a new source:
   - accept the source from chat or `inbox/sources/`
   - preserve the raw excerpt or file in `raw/`
   - create or update a source summary in `sources/`
   - promote its durable insights into the correct long-term destination
   - update `index.md` and append an entry to `log.md`
3. For a question:
   - answer from existing wiki pages first
   - cite the specific pages used
   - if the answer is worth keeping, file it into `queries/` or directly into its canonical destination
   - update `index.md` and `log.md`
4. For a research topic:
   - start in `research/` when the topic is unresolved or source-heavy
   - promote the stable parts into `knowledge/` when understanding becomes durable
5. For a maintenance pass:
   - look for contradictions
   - look for stale claims superseded by newer sources
   - look for orphan pages and weak links
   - look for research dossiers ready to be promoted to evergreen pages
   - look for ideas or saved queries that should be normalized

## Domain-Specific Rules

- Blood work:
  - keep raw lab material under `raw/health/`
  - keep dated interpretation and feedback under `records/health/blood-work/`
  - maintain at least one longitudinal view that tracks notable markers over time
- Finance:
  - use `records/finance/` for major versioned plans such as `v1`, `v2`, and `v3`
  - retain context from previous iterations inside the current version page
- Recipes:
  - store them under `reference/health/nutrition/recipes/`
  - include macros when available
- Tweets, podcast snippets, and Kobo highlights:
  - preserve the raw excerpt locally
  - use digests when many small fragments inform the same topic
- Ideas:
  - favor low-friction capture under `ideas/`
  - only normalize into other areas when the idea matures
- Company-building:
  - keep reusable general knowledge in this repository
  - reserve separate project repos for project-specific execution context later

## Writing Rules

- Use markdown only.
- Prefer short sections and explicit headings over long prose.
- Use Obsidian wikilinks between related pages.
- Keep claims traceable by linking back to `sources/` or `records/` pages.
- If two sources disagree, record the disagreement rather than collapsing it.
- When unsure, mark a claim as tentative.
- Avoid duplicating full source text in the wiki layer. Summarize and synthesize instead.

## Frontmatter Conventions

Use YAML frontmatter when practical.

Common fields:

- `type`
- `title`
- `status`
- `created`
- `updated`
- `tags`

Helpful type-specific fields:

- `raw-source`: `author`, `captured`, `source_type`, `url`
- `source-summary`: `author`, `published`, `ingested`, `raw_source`
- `evergreen`: `source_pages`
- `research-dossier`: `focus`, `source_pages`
- `record`: `recorded_on`, `source_pages`
- `query`: `question`, `answered_on`, `based_on`

## Naming Conventions

- Raw captures: `YYYY-MM-DD short-slug.md`
- Source summaries: `YYYY-MM-DD Source Title.md`
- Saved queries: `YYYY-MM-DD Short Question.md`
- Evergreen pages, references, and dossiers: natural titles
- Finance plans: `YYYY-MM-DD Finance Plan vN.md`
- Blood work records: `YYYY-MM-DD Blood Work.md`

## Non-Goals

- Do not turn the wiki into a dumping ground of raw excerpts.
- Do not overfit the folder tree before usage proves the need.
- Do not silently delete historical reasoning.
- Do not create many tiny standalone pages when one digest or evergreen page would be cleaner.
