---
type: overview
title: LLM Wiki Overview
status: active
updated: 2026-05-05
tags:
  - overview
  - llm-wiki
  - personal-os
---

# LLM Wiki Overview

## Current State

This repository is a Personal OS built on the LLM wiki pattern and intended to be maintained primarily through Codex.

It now includes a staged import of the user's prior Obsidian reading vault: book highlights, long-form web highlights, and a small set of personal notes. Those captures live in the raw layer and should be promoted gradually into summaries, evergreen pages, research dossiers, references, records, or idea notes.

## Working Assumptions

- Obsidian is the browsing and editing interface.
- Codex is responsible for most maintenance work: summarizing, cross-linking, updating, normalizing, and filing.
- Raw source captures stay under `raw/` and are not rewritten during synthesis.
- Imported reading highlights are source material, not finished synthesis.
- Fast intake can happen through chat or `inbox/sources/`.
- Durable knowledge lives in `knowledge/`, `records/`, `reference/`, `research/`, `ideas/`, `sources/`, and `queries/`.

## Recommended First Use

- Ingest one source you already care about.
- Convert one existing book note into a richer maintained page under `knowledge/reading-writing/books/`.
- Add one small social or podcast fragment and let Codex fold it into a digest.
- Add one blood work or finance artifact and confirm the record workflow feels right.
- Ask one synthesis question that requires more than a single source page.

## Core Domains

- `health`
- `company-building`
- `ai-agents`
- `finance`
- `reading-writing`
- `travel`
- `philosophy-politics`

## Important Object Types

- evergreen knowledge pages
- research dossiers
- historical records
- versioned finance plans
- practical reference pages
- high-volume idea capture
