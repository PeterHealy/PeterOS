---
type: reference
title: "Local LLM Setup"
status: active
created: 2026-05-07
updated: 2026-05-07
source_pages:
  - "[[sources/ai-agents/Zeneca - All About Local LLMs]]"
  - "[[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]"
tags:
  - reference
  - ai-agents
  - local-llms
  - tools
---

# Local LLM Setup

## Default Stack

- Use [[reference/Tools And Websites|LM Studio]] to browse, download, and test models through a desktop UI.
- Use [[reference/Tools And Websites|Ollama]] for scripts, agents, and always-on local API workflows.
- Use [[reference/Tools And Websites|llama.cpp]] or `llama-server` when lower-level control and model fit matter more than GUI convenience.
- Use [[reference/Tools And Websites|llama-swap]] when multiple local models need to be exposed behind a stable local endpoint.
- Use [[reference/Tools And Websites|Hugging Face]] as the broader model catalog.
- Prefer Q4 quantized models unless there is a specific reason to trade memory or speed for quality.

## Hardware Selection

- Existing Apple Silicon laptop: good enough for trying small local models.
- Existing PC: a used RTX 3090 can be a cost-effective VRAM upgrade.
- Small-to-medium models with speed as the priority: NVIDIA workstation with RTX 4090 or 5090.
- 30B+ models, quiet operation, or always-on local inference: high-memory Mac Mini Pro or Mac Studio.
- Largest open-weight models: high-unified-memory Mac Studio or a much more expensive multi-GPU workstation.

## Agent Endpoints

Common local OpenAI-compatible endpoints:

- Ollama: `http://localhost:11434/v1`
- LM Studio: `http://localhost:1234/v1`

Use these when an agent framework supports custom OpenAI-compatible providers.

## Security Defaults

- Do not give a local agent raw access to email, messaging, wallets, or account-changing APIs.
- Wrap sensitive capabilities in narrow local tools or daemons with explicit guardrails.
- Require human confirmation for outbound messages, transfers, publishing, account changes, installs, and other high-risk actions.
- Keep private local context and untrusted internet content in separate execution paths when possible.
- Sanitize private details locally before calling stronger remote models.

## Model Choice Rule

Pick the smallest model that is good enough for the task. This keeps latency, memory pressure, and hardware requirements lower while preserving local-model advantages.

## Related

- [[knowledge/ai-agents/Local LLM Operating Model]]
- [[knowledge/ai-agents/Secure Local AI Agent Architecture]]
- [[sources/ai-agents/Zeneca - All About Local LLMs]]
- [[sources/ai-agents/Vitalik Buterin - My Self-Sovereign Local Private Secure LLM Setup]]
