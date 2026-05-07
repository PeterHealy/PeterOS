---
type: source-summary
title: "Packy McCormick and Pim De Witte - World Models: Computing the Uncomputable"
author: Packy McCormick and Pim De Witte
published: 2026-03-19
ingested: 2026-05-07
status: processed
url: https://www.notboring.co/p/world-models
summary_basis: full source URL plus user-provided excerpts
raw_source: "[[raw/ai-agents/not-boring-world-models-highlight-capture]]"
tags:
  - ai-agents
  - world-models
  - embodied-ai
  - robotics
  - games
---

# Packy McCormick and Pim De Witte - World Models: Computing the Uncomputable

## Summary Basis

- URL: https://www.notboring.co/p/world-models
- Based on: full source URL, read on 2026-05-07, plus the user's submitted excerpts.
- Raw capture: [[raw/ai-agents/not-boring-world-models-highlight-capture]]

## What This Source Is

A long Not Boring essay co-written by Packy McCormick and General Intuition co-founder Pim De Witte. It argues that world models are a distinct foundation-model path for embodied AI because they learn action-conditioned dynamics: not just what a scene might look like next, but what happens when an agent intervenes.

## Source Summary

The essay's starting point is that humans can imagine complex future scenes with roughly fixed subjective effort, while hand-coded simulation gets more expensive as objects, people, interactions, and edge cases multiply. World models are presented as a learned alternative: after training, a dynamic scene can be advanced through a neural forward pass rather than through explicit calculation of every entity and pairwise interaction.

The authors distinguish world models from ordinary video models. A video model predicts plausible visual continuation; a world model predicts the next state conditional on an action. That distinction makes interactivity central. The authors frame actions as an especially dense compression of perception, planning, hidden state, intent, and consequence: an observer does not need to know all the cognition behind a person avoiding a puddle if the action plus outcome can be observed.

The technical argument emphasizes latent prediction. Instead of predicting every pixel, modern world models can encode observations into compact representations and predict the next latent state under an action. Good world models must also represent stochasticity: both reducible ignorance about unseen patterns and irreducible randomness about which valid future occurs. Naive averaging over multiple futures produces implausible "blurry" predictions, so world models need ways to preserve possible futures rather than collapse them into a mean.

The essay places the idea in a long lineage: simulation philosophy, Schmidhuber's 1990 proposal to train agents inside learned worlds, Sutton's Dyna architecture, and Ha and Schmidhuber's 2018 `World Models` paper with vision, memory, and controller components. It then argues that language and code alone are too lossy or too rule-bound to solve physical, spatial, and temporal intelligence. To know the world, an agent must interact with it or learn from observed interaction.

Games are central because they provide what the real world rarely does at scale: labeled spatial-temporal data, clear action-outcome pairs, consistent physics, reward signals, and controlled environments for repeated experimentation. The essay walks through successive waves of progress, including Dreamer, MuZero, IRIS, GAIA-1, DIAMOND, GAIA-2, Genie, Sora/Veo-style video models, comma.ai's world-model-trained driving policy, Meta's V-JEPA 2, and Google DeepMind's SIMA 2.

The current field is presented as three overlapping approaches: current foundation models used as substrates, specialized world models, and embodied agents. Open questions include whether LLM/VLA systems can substitute for dedicated world models, how much action can be inferred from video, whether latent prediction beats pixel generation for planning, and which learned simulations transfer to real robots or vehicles.

General Intuition's specific thesis is that action-labeled gaming clips are a rare data advantage. Medal contributes large volumes of game clips enriched with in-game action metadata, letting models connect what a player saw to the actions that followed. The authors argue that focusing on controller-like interfaces and vision can reduce two transfer problems: input-modality transfer and sensor transfer. The remaining hard problem is environment transfer: whether agents trained in game-like dreams operate reliably in reality.

The essay closes with a strong claim against humanoid maximalism. If useful machines can be controlled through simple, already-optimized interfaces such as wheels, joysticks, keyboards, and gamepads, then robotics may progress faster through cheaper task-specific machines than through human-shaped bodies. World models matter because they may let agents learn the cause-and-effect structure behind those interfaces and act in real environments.

## Key Ideas

- A world model is action-conditioned: it models `next state given current state and action`, not merely `next frame given current frame`.
- Actions compress perception, intent, hidden context, and downstream consequence into a training signal.
- Latent state prediction is cheaper than raw-pixel prediction and can preserve the information needed for planning.
- A useful world model must handle multiple possible futures rather than average them into an impossible middle.
- Games are unusually good training environments because they pair observations, actions, rewards, and outcomes at scale.
- The dream-to-reality loop is the central promise: train or improve an agent inside a learned world, then transfer the learned policy back to a real environment.
- The field is still unsettled; foundation-model agents, latent world models, generative video/world models, and embodied policies may converge or compete.
- General Intuition's bet is shaped by Medal's data: massive action-labeled gameplay can become a bridge toward controlling machines through controller-like interfaces.

## Claims Worth Tracking

- World models may provide a better path than language-only systems for embodied AI and robotics.
- Scaling laws appear to apply to visual/world-model systems, but real-world transfer laws are less understood.
- Ground-truth action labels are materially better than inferred actions, especially for edge cases.
- Video models are not enough unless they become interactive, action-conditioned systems.
- Humanoid robots may be an overfit to internet-video data availability rather than the most practical machine form factor.
- The main transfer curves to watch are input modality, sensor, and environment transfer.
- World models can be economically important not only as robot brains but also as a way to use distributed gaming hardware and human teleoperation capacity.

## Your Captures

No explicit PNote annotations were included in the submitted capture. The full submitted excerpts are preserved in [[raw/ai-agents/not-boring-world-models-highlight-capture]].

## Capture-Based Synthesis

- The excerpt selection highlights the idea that human imagination skips explicit simulation while remaining good enough to plan.
- The latent-space passage frames prediction efficiency as compression: encode frames into compact state, predict state transitions, and avoid wasting compute on unchanged pixels.
- The stochasticity passage emphasizes uncertainty, especially the failure mode where naive prediction averages valid futures into an invalid one.
- The actions-as-compression passage makes behavior useful because actions reveal the output of hidden internal calculation.
- The games passage is a data lesson: games are useful not because games are important, but because they expose action-outcome data that the real world usually hides.

## Caveats

- The essay is co-written with a founder of General Intuition, so it is partly an explanatory market map and partly a company thesis.
- The article makes strong claims about transfer from games to reality; those claims should be treated as provisional until more public deployment evidence exists.
- Funding rounds and model names reflect the state of the field around March 2026 and should be refreshed before being used as current market data.
- Several cited systems are research prototypes, not stable production platforms.

## What Changed In The Wiki

- Added [[knowledge/ai-agents/README]] as the start of the AI-agent knowledge domain.
- Added [[knowledge/ai-agents/World Models]] as an evergreen page for the concept, data requirements, distinctions, and open questions.
- Updated [[reference/Tools And Websites]] with reusable AI-agent and robotics resources mentioned in the source.

## Open Questions

- Which approach transfers best to the physical world: latent prediction, generative diffusion world models, VLA-style foundation-model agents, or direct policy learning from experience?
- How much action information can be reliably inferred from ordinary video, and where does inferred action break?
- Are controller-like action spaces enough for broad robotics, or do high-degree-of-freedom humanoid tasks require a different data strategy?
- What benchmarks will make environment transfer visible before companies spend huge sums collecting physical robot data?
- How should safety, labor displacement, and shared economic upside be designed if world-model agents become broadly useful?

## Related Pages

- [[knowledge/ai-agents/World Models]]
- [[raw/ai-agents/not-boring-world-models-highlight-capture]]
- [[reference/Tools And Websites]]
