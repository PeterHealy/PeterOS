---
type: reference
title: ETHSkills
status: active
created: 2026-04-19
updated: 2026-04-19
tags:
  - ai-agents
  - skills
  - ethereum
  - reference
---

# ETHSkills

## What It Is

A public skill library for AI agents working on Ethereum. It is designed to give agents current, domain-specific guidance by letting them fetch markdown skills on demand.

## Why Keep It

- It is a strong example of an external skill resource.
- It uses a simple URL-addressable `SKILL.md` pattern.
- It can be useful whenever an agent is working on Ethereum, wallets, L2s, Solidity, gas, security, or deployment.

## Structure

- top-level `SKILL.md` for routing
- domain-specific sub-skills such as `ship`, `protocol`, `gas`, `wallets`, `l2s`, `standards`, `tools`, `security`, `testing`, `frontend-ux`, `qa`, and `audit`

## How To Use It

- Start with `https://ethskills.com/SKILL.md`
- Fetch narrower skill pages only when needed
- Treat it as a live domain reference rather than static local documentation

## Why This Matters For PeterOS

- It justifies a dedicated `skills` section for agent-oriented resources.
- It shows that some references are aimed at helping agents perform work, not just helping humans understand a topic.
- It provides a pattern we can reuse for other strong external skill libraries later.

## Canonical Source

- [[sources/ai-agents/2026-04-19 ETHSkills]]
- <https://ethskills.com/>
