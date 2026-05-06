---
type: source-summary
title: ETHSkills
author: Austin Griffith
published:
ingested: 2026-04-19
status: processed
raw_source: "[[raw/ai-agents/ethskills]]"
tags:
  - ai-agents
  - skills
  - ethereum
  - reference
---

# ETHSkills

## What This Source Is

A public skill library for AI agents that need current Ethereum knowledge. Instead of installing a package, the agent fetches markdown skill files on demand from `ethskills.com`.

## Key Ideas

- Skill resources can be external, URL-addressable, and agent-readable.
- A top-level `SKILL.md` can route the agent to more specific sub-skills only when needed.
- The library is opinionated about a narrow domain and is designed to correct stale model knowledge with current operational guidance.

## Claims Worth Tracking

- External skill libraries are a useful object type inside PeterOS, separate from general articles or playbooks.
- The "fetch markdown on demand" model is a strong pattern for domain-specific agent guidance.
- Skill libraries can contain both conceptual knowledge and operational checklists.

## Caveats

- This is an external resource, not a local installed skill in PeterOS.
- It is domain-specific to Ethereum and onchain building.
- Live skill content can change over time, so the local note should summarize the role of the resource rather than pretending to be a frozen mirror.

## What Changed In The Wiki

- Added a raw metadata stub under `raw/ai-agents/`.
- Added a dedicated `reference/ai-agents/skills/` area for external skill libraries.
- Added a reusable reference note at [[reference/ai-agents/skills/ETHSkills]].

## Open Questions

- Should PeterOS also hold internal house skills or only references to external skill libraries?
- Which other agent skill libraries deserve to live next to ETHSkills?
- When should a skill reference be promoted into a more general knowledge page?

## Related Pages

- [[reference/ai-agents/skills/ETHSkills]]
- [[reference/ai-agents/skills/README]]
