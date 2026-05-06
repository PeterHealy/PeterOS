---
type: reference
title: Minimalist Entrepreneur Skills
status: active
created: 2026-04-27
updated: 2026-04-27
tags:
  - ai-agents
  - skills
  - company-building
  - startup
  - reference
---

# Minimalist Entrepreneur Skills

## What It Is

An external skill library that packages a founder methodology into agent-usable markdown skills. It is most relevant when thinking through business ideas, validation, MVP scope, manual-first delivery, pricing, first customers, and sustainable growth.

## Why Keep It

- It is a good example of a non-technical skill library: the agent is being given judgment heuristics, not API knowledge.
- It shows a clean pattern for turning a book or operating philosophy into reusable agent prompts.
- It may be more useful as a repeatable decision lens than as prose notes.

## Structure

- Claude plugin metadata under `.claude-plugin/`
- 10 skill directories under `skills/`
- one `SKILL.md` per skill, each focused on a recurring founder question

## How To Use It

- Use it when you want an opinionated minimalist-founder lens on a business decision.
- Do not vendor it into PeterOS by default.
- If a specific skill repeatedly changes your behavior, extract the durable principle into `reference/company-building/` or `knowledge/company-building/`.
- If you actually want to run the skills, install them in the agent environment rather than storing them in the wiki.

## Best Fit In This Repo

- Keep the repo itself as an external reference.
- Treat the underlying heuristics as candidate source material for company-building notes.
- Avoid copying the full skill text into the wiki unless you are deliberately adapting one skill into your own house process.

## Canonical Source

- [[sources/ai-agents/Sahil Lavingia - Minimalist Entrepreneur Skills]]
- <https://github.com/slavingia/skills>
