---
type: source-summary
title: "Zeneca - All About Local LLMs"
status: active
created: 2026-05-07
updated: 2026-05-07
author: Zeneca
published: 2026-04-21
ingested: 2026-05-07
url: https://www.zeneca.xyz/p/letter-109-all-about-local-llms
summary_basis: full source
raw_source: "[[raw/ai-agents/zeneca-all-about-local-llms-highlight-capture]]"
tags:
  - source-summary
  - ai-agents
  - local-llms
  - hardware
---

# Zeneca - All About Local LLMs

## Summary Basis

Full source. The canonical article was accessible during ingest, so this summary is based on the full article rather than only the highlighted excerpts.

## Core Argument

Local LLMs are now useful enough to be part of a normal AI workflow, even if they do not replace frontier cloud models. Zeneca's recommended pattern is hybrid: use cloud models for the hardest reasoning and coding tasks, and local models for privacy-sensitive, everyday, offline, low-cost, or rate-limit-free work.

The hardware constraint is mostly memory, not raw compute. Quantization makes models smaller, with Q4 presented as the practical default. A rough rule of thumb from the article is that a Q4 model needs about 0.6-0.7 GB of memory per billion parameters.

## Hardware Takeaways

- Small and medium local models are fastest on NVIDIA GPUs when the model fits in VRAM.
- Large models are where Macs become attractive because unified memory lets the whole model sit in one shared memory pool.
- Consumer NVIDIA cards have much smaller VRAM pools than high-end Mac unified-memory configurations, so once a model spills beyond VRAM, moving data between GPU and system RAM becomes the bottleneck.
- Power and noise matter for always-on inference: the article frames Mac Studio as dramatically quieter and more power-efficient than an RTX 4090 workstation.
- For budget experimentation, a used RTX 3090 is positioned as strong value per GB of VRAM.
- For a quiet all-in-one machine or 30B+ models, the article recommends higher-memory Apple Silicon machines.

## Software Stack

- [[reference/Tools And Websites|LM Studio]] is recommended as the easiest starting point for non-developers because it provides a GUI, model discovery, and RAM fit indicators.
- [[reference/Tools And Websites|Ollama]] is framed as better for developers and agent workflows because it runs as a background service, exposes local API endpoints, and is simpler to script.
- Hugging Face is the model repository layer.
- llama.cpp and MLX are the lower-level inference engines most users can ignore.
- Unsloth is mentioned as a route into fine-tuning local models on personal data or writing style.

## Model Selection Heuristic

The practical question is not "what is the best model?" but "what is the smallest model that handles this task well enough?"

As of 2026-04-21, Zeneca highlights Kimi K2.6 and GLM-5.1 as top-tier open-weight coding models, while Qwen3.6-35B-A3B is presented as a likely sweet spot for more normal hardware. Smaller models such as Qwen 3.5 9B are framed as useful for email rewriting, article summarization, and quick Q&A on low-memory devices.

## Agent Workflow

The article treats local chat as useful, but local models connected to agents as the more interesting unlock. Ollama and LM Studio expose OpenAI-compatible endpoints, which means local models can be connected to agent frameworks that accept custom OpenAI-style providers.

Example local endpoints from the article:

- Ollama: `http://localhost:11434/v1`
- LM Studio: `http://localhost:1234/v1`

## Your Captures

The submitted capture included two highlighted passages and no separate PNote annotations.

### Highlight 1

> For large models (30B+), Macs win. Here’s why: NVIDIA consumer GPUs max out at 24 GB of VRAM (4090) or 32 GB (5090). Once your model exceeds that, the GPU has to shuttle data back and forth with system RAM over a slow connection, and performance suffers as a result. The Mac isn’t faster because Apple chips are faster, the Mac is faster because the whole model fits in memory at once.

### Highlight 2

> A Mac Studio pulls about 60W under full load. An RTX 4090 pulls 450W plus whatever the rest of the PC uses. If you’re running inference all day, the electricity costs will add up over time. Macs are also silent. PC workstations with 4090s are LOUD. My Mac Studio sits on my desk and I rarely hear a thing from it.

## Durable Links

- [[knowledge/ai-agents/Local LLM Operating Model]]
- [[reference/ai-agents/Local LLM Setup]]
- [[reference/Tools And Websites]]
