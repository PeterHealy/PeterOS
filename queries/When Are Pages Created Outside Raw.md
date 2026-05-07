---
type: query
title: When Are Pages Created Outside Raw?
status: active
created: 2026-05-07
updated: 2026-05-07
question: When are things made outside of raw?
answered_on: 2026-05-07
based_on:
  - "[[AGENTS]]"
  - "[[index]]"
tags:
  - query
  - llm-wiki
  - maintenance
---

# When Are Pages Created Outside Raw?

## Short Answer

`raw/` is created when something needs to be preserved as source material.

Everything outside `raw/` is created when that source material, a question, or a repeated need becomes useful enough to interpret, summarize, reuse, track, or act on.

The raw page answers: what was captured?

The non-raw page answers one of these:

- What does this source mean?
- What durable thing do I now believe or know?
- What should I do with this?
- What is still unresolved?
- What changed over time?
- What answer is worth keeping?

## What Gets Created After A Submission

For a normal `[SUBMIT]` source, the default path is:

1. Create a `raw/` page to preserve the original capture.
2. Create or update a `sources/` page to summarize the source.
3. Promote durable insights into `knowledge/`, `reference/`, `research/`, `ideas/`, or `records/` when warranted.
4. Update [[index]].
5. Append [[log]].

Not every submission needs a new page in every folder.

## Folder Rules

### `sources/`

Create a page in `sources/` when a source is important enough to have a human-readable summary or digest.

Use this for:

- article summaries
- book highlight digests
- tweet or podcast digests
- video notes
- tool or website summaries

This is usually the first non-raw page after an ingest.

### `knowledge/`

Create or update a page in `knowledge/` when the material produces durable understanding.

Use this when a source changes or strengthens a reusable model, principle, thesis, or explanation.

Examples:

- a theory about agent-native startups
- a writing principle
- a finance heuristic
- a health model
- a philosophy or worldview idea

Do not create a new evergreen page for every source. Prefer updating an existing page when the idea belongs there.

### `reference/`

Create or update a page in `reference/` when the material is practical lookup material.

Use this for:

- checklists
- recipes
- protocols
- supplements
- visa notes
- tools and websites
- reusable workflows
- implementation guides

If the thing is something you might use while doing a task, it probably belongs in `reference/`.

### `research/`

Create or update a page in `research/` when the topic is unresolved, source-heavy, or still messy.

Use this when:

- several sources are accumulating around one open question
- there are contradictions
- the idea is interesting but not yet stable
- the topic might later become evergreen knowledge

Research pages are allowed to be provisional.

### `records/`

Create a page in `records/` when the material is dated, versioned, or longitudinal.

Use this for:

- blood work
- finance plans
- snapshots
- personal state records
- manifests
- versioned strategy documents

Records preserve what was true at a point in time.

### `ideas/`

Create a page in `ideas/` when the material is a user-originated idea, build concept, writing seed, or speculative thought.

Use this when the value is optionality rather than truth.

Ideas can be rough. They only get normalized later if they mature.

### `queries/`

Create a page in `queries/` when a question-answer pair is likely to be useful again.

Use this for:

- operating answers
- decision memos
- synthesis answers
- comparisons
- reusable explanations

If the answer belongs directly inside a canonical `knowledge/`, `reference/`, or `research/` page, file it there instead.

### `inbox/outputs/`

Use `inbox/outputs/` when an answer is useful but not yet normalized.

This is a temporary staging area, not a permanent home.

## Practical Decision Rule

Ask what job the new page is doing:

- Preserve original material: `raw/`
- Summarize one source: `sources/`
- Store durable understanding: `knowledge/`
- Store a practical lookup or workflow: `reference/`
- Work through an unresolved topic: `research/`
- Track dated or versioned state: `records/`
- Capture optional ideas: `ideas/`
- Save a reusable answer: `queries/`
- Hold something useful but unfiled: `inbox/outputs/`

## What Should Not Happen

Do not create non-raw pages just because a raw page exists.

Do not create many tiny evergreen pages when one digest or existing evergreen page would be cleaner.

Do not duplicate the full source text outside `raw/`.

Do not silently replace older reasoning. If newer material changes the view, record the change.

