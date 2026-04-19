---
type: source-summary
title: LLM Wiki
author: Andrej Karpathy
published: 2026-04-04
ingested: 2026-04-18
status: processed
raw_source: "[[raw/misc/2026-04-18 karpathy-llm-wiki]]"
tags:
  - llm-wiki
  - knowledge-base
  - obsidian
---

# LLM Wiki

## Core Claim

Instead of answering questions by repeatedly retrieving fragments from raw documents, an LLM can maintain a persistent interlinked markdown wiki that accumulates synthesis over time.

## Architecture

- Raw sources remain the source of truth and are not modified.
- The wiki is an LLM-maintained layer of summaries, entities, concepts, comparisons, and syntheses.
- A schema file guides the LLM on structure, naming, and maintenance workflows.

## Operating Loops

- Ingest sources one at a time or in batches, then update all affected pages.
- Answer questions against the compiled wiki, not just the raw source set.
- Save valuable answers back into the wiki.
- Periodically lint the wiki for contradictions, stale claims, orphan pages, and missing pages.

## Obsidian-Specific Takeaways

- Obsidian works well as the browsing interface because the LLM can maintain markdown while the user follows links and graph structure.
- `index.md` and `log.md` are important navigation files and reduce the need for heavier retrieval tooling at small to medium scale.
- Dataview, local assets, and markdown-first tools fit naturally into this workflow.

## Implications For This Repository

- The repository should be treated as a living vault, not a document dump.
- Every meaningful ingest should update `index.md` and `log.md`.
- Durable knowledge should move from `sources/` into `knowledge/`, `records/`, `reference/`, `research/`, `ideas/`, and `queries/`.

## Related Pages

- [[knowledge/meta/LLM Wiki Pattern]]
- [[overview]]
