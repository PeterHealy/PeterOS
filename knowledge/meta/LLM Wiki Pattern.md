---
type: evergreen
title: LLM Wiki Pattern
status: active
updated: 2026-04-19
source_pages:
  - "[[sources/misc/Karpathy - LLM Wiki]]"
tags:
  - llm-wiki
  - workflow
  - obsidian
  - meta
---

# LLM Wiki Pattern

## Definition

A workflow where the LLM maintains a persistent interlinked markdown wiki instead of rediscovering knowledge from raw documents at query time.

## Why It Matters

- Knowledge compounds instead of resetting every time a question is asked.
- The wiki captures synthesis, cross-links, and contradictions ahead of time.
- The maintenance burden shifts from the human to the LLM.

## Minimal Operating Model

- Add raw sources under `raw/`.
- Summarize each source under `sources/`.
- Update long-lived pages under `knowledge/`, `records/`, `reference/`, `research/`, `ideas/`, and `queries/` as needed.
- Keep `index.md`, `log.md`, and `overview.md` current.

## Fit For This Repository

- Obsidian is a strong fit for browsing and graph navigation.
- Books can be first-class pages inside `knowledge/reading-writing/books/`.
- The highest-value automation is maintenance work: summaries, cross-links, synthesis, and filing.

## Open Design Choices

- Keep this as a separate vault or merge it into the existing `Notes` vault.
- Decide how much of the current `Books` workflow should remain manual versus LLM-maintained.
- Decide which active domains deserve separate project repos later and which should stay in the main Personal OS.
