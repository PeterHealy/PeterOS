---
type: evergreen
title: "Local LLM Operating Model"
status: active
created: 2026-05-07
updated: 2026-05-07
source_pages:
  - "[[sources/ai-agents/Zeneca - All About Local LLMs]]"
  - "[[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]"
tags:
  - evergreen
  - ai-agents
  - local-llms
---

# Local LLM Operating Model

## Working Model

Local LLMs are best treated as a complement to frontier cloud models, not a full replacement. Use frontier models for high-stakes reasoning, hard multi-step coding, and tasks where maximum quality matters. Use local models for privacy-sensitive inputs, cheap repeated work, offline access, rate-limit avoidance, and always-on background workflows.

## Hardware Principle

Available memory is the main constraint. For PCs, that means VRAM. For Macs, that means unified memory. Small and medium models that fit in NVIDIA VRAM can be very fast, but large models that exceed consumer GPU VRAM can slow down sharply when data has to move between GPU and system memory.

Apple Silicon is attractive for larger local models because unified memory allows a bigger model to fit into one shared pool. The important distinction is not "Mac chips are faster"; it is "the whole model can remain resident in memory."

## Practical Heuristic

Ask: what is the smallest local model that handles this job well enough?

- Use small models for rewriting, summarization, Q&A, extraction, and simple scripting.
- Use medium models when code context, document length, or quality requirements increase.
- Reserve very large local models for workflows where privacy, autonomy, or sustained local operation justify the hardware cost.

## When Local Wins

- Sensitive documents, proprietary code, or private personal data should not leave the machine.
- Repetitive jobs can run without API usage costs or subscription rate limits.
- Offline or unreliable-network contexts still have access to a useful assistant.
- Agent workflows can run against local OpenAI-compatible endpoints.
- Always-on local services avoid cloud dependency and provider policy changes.

## Security Boundary

Local inference is not the same as secure agency. A local model with broad file, network, email, wallet, and shell access can still leak data or take harmful actions if it is confused by hostile content or wrapped in unsafe tools.

For agent workflows, use a least-permission setup:

- keep private data and untrusted internet content separated where possible
- expose sensitive systems through narrow wrapper tools or local daemons
- require human confirmation for messages, payments, account changes, publishing, and other high-risk external actions
- allow remote models only the minimum sanitized subproblem they need to solve

## When Cloud Still Wins

- Frontier reasoning and difficult multi-file coding remain better served by top cloud models.
- Hosted models avoid large local hardware purchases.
- Cloud tools usually have better polished interfaces, collaboration features, and managed updates.

## Operating Pattern

Maintain a hybrid stack:

- Cloud for the hardest tasks.
- Local for routine, private, offline, or background tasks.
- GUI tools for model discovery and testing.
- Headless local APIs for agents, scripts, and scheduled workflows.

## Related

- [[sources/ai-agents/Zeneca - All About Local LLMs]]
- [[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]
- [[knowledge/ai-agents/Secure Local AI Agent Architecture]]
- [[reference/ai-agents/Local LLM Setup]]
- [[reference/Tools And Websites]]
