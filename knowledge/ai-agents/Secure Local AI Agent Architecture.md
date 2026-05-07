---
type: evergreen
title: "Secure Local AI Agent Architecture"
status: active
created: 2026-05-07
updated: 2026-05-07
source_pages:
  - "[[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]"
tags:
  - evergreen
  - ai-agents
  - local-llms
  - security
  - privacy
---

# Secure Local AI Agent Architecture

## Core Principle

A local AI agent is only private and secure if its permissions are constrained. Running inference locally helps, but it does not solve prompt injection, malicious tools, data exfiltration, wallet abuse, accidental posting, or model backdoors by itself.

Treat the agent as a powerful local process that should receive only the data, network access, and action rights needed for the current job.

## Trust Zones

Separate these zones whenever possible:

- private local files and messages
- untrusted internet content
- model inference
- tool execution
- external communication channels
- payment, wallet, or account-changing actions

The riskiest setup is one where the same agent can read private data, browse hostile content, access the internet, and take irreversible external actions without confirmation.

## Mediated Tool Access

Expose sensitive capabilities through narrow local daemons or wrapper tools instead of raw account access.

Good mediated tools should:

- allow specific low-risk operations
- block or require confirmation for high-risk operations
- make exfiltration harder by constraining destinations, amounts, calldata, recipients, or message contexts
- provide logs that a human can inspect
- keep unrelated account capabilities out of the agent's reach

## Confirmation Boundary

For high-risk actions, require both the human and the LLM to approve. The useful security property is that humans and LLMs fail in different ways.

Examples that should usually cross a confirmation boundary:

- sending email or messages
- publishing content
- transferring money or crypto assets
- changing account settings
- installing or executing untrusted code
- sending private data to a new external destination

Low-risk actions can be smoother, but the low-risk category should be defined narrowly.

## Remote AI Boundary

Local models will not always be strong enough. When using remote models, reduce leakage in layers:

- strip private details locally before sending a request
- split tasks so the remote model sees only the hard subproblem
- avoid linking requests to persistent identities when possible
- route traffic through privacy-preserving network layers when practical
- prefer verifiable confidential inference when it is available and actually verified locally

## Working Heuristic

The question is not "local or cloud?" The question is:

What is the least-permissive architecture that lets the agent complete the task?

Use local inference and local files as the default for private context. Use remote intelligence selectively for hard subproblems. Keep risky actions behind mediated tools and explicit confirmation.

## Related

- [[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]
- [[knowledge/ai-agents/Local LLM Operating Model]]
- [[reference/ai-agents/Local LLM Setup]]
