---
type: evergreen
title: World Models
status: active
created: 2026-05-07
updated: 2026-05-07
source_pages:
  - "[[sources/ai-agents/Packy McCormick and Pim De Witte - World Models Computing the Uncomputable]]"
  - "[[sources/ai-agents/Packy McCormick and Evan Beard - Many Small Steps for Robots]]"
tags:
  - ai-agents
  - world-models
  - embodied-ai
  - robotics
  - games
---

# World Models

## Working Definition

A world model is a learned model of environment dynamics that predicts future states conditional on actions.

The important distinction is interactivity. A video model predicts plausible continuation from previous frames. A world model predicts what changes when an agent acts. In shorthand:

- Video model: next observation given previous observation.
- World model: next state given current state and action.

## Why They Matter

- They offer a path for agents to plan in spatial-temporal environments, not only reason in language.
- They can reduce complex hand-coded simulation into learned inference after training.
- They let an agent practice inside a synthetic environment, then test or deploy the learned policy in the real one.
- They may be especially important for robotics, autonomous vehicles, game agents, and other embodied systems where the world responds to actions.

## Core Components

- Observation encoder: compresses pixels, sensor readings, or other observations into a latent state.
- Dynamics model: predicts how that latent state evolves under an action.
- Policy or controller: chooses actions using the current state and predicted futures.
- Training data: pairs observations with actions and outcomes.
- Evaluation loop: compares imagined futures or learned policies against real outcomes.

## Actions As Compression

Actions compress a large hidden calculation into a visible signal. A person stepping left may encode perception, intent, preference, body state, urgency, risk tolerance, and prediction about nearby people or objects. A model observing the action and consequence can learn from the output of that calculation without seeing the full internal reasoning.

This is why action labels matter. Ordinary video shows what happened. Action-labeled video shows what happened because an agent did something.

## Uncertainty

World models need to represent multiple possible futures.

- Epistemic uncertainty: the model has not yet learned enough about the environment.
- Aleatoric uncertainty: the environment contains inherent randomness or multiple valid futures.

A model that averages all possible futures can produce impossible middle states. For planning, the model must preserve plausible alternatives instead of collapsing them into a blur.

## Distinctions

- A video model is not necessarily a world model because it may be non-interactive.
- A 3D reconstruction model is not necessarily a world model because geometry alone does not model action-conditioned dynamics.
- An LLM can hold causal facts about the world, but language alone is a lossy abstraction of spatial-temporal reality.
- A hand-coded simulator can be precise inside its rules, but it struggles with open-ended stochastic environments unless the relevant dynamics are already specified.

## Data Lessons

Games are unusually useful because they expose:

- observations
- actions
- outcomes
- reward signals
- repeatable environments
- controlled experiments at massive scale

The real world has richer stakes but worse labels. It is harder to know exactly what action caused what outcome, harder to run dangerous or rare cases, and harder to observe hidden state.

For deployed robotics, ordinary video and simulation also miss parts of the physical interaction that matter for control: force, torque, friction, compliance, stiffness, contact dynamics, and hardware-specific sensor feedback. [[knowledge/ai-agents/Robotics Data And Deployment Gradient]] treats this as the embodiment gap: useful world models for robots need to be grounded in data from the body and task they will actually control.

## Transfer Questions

The practical challenge is transfer: can an agent trained in a learned world act reliably outside it?

Three transfer curves matter:

- Input modality transfer: whether a policy trained on one control interface applies to another.
- Sensor transfer: whether a model trained on one observation stream can use another.
- Environment transfer: whether performance holds as environments become more complex, stochastic, populated, or out-of-distribution.

## Practical Heuristics

- Prefer ground-truth action labels over inferred actions when reliability matters.
- Treat pure video generation as adjacent but insufficient until it supports intervention.
- Use the real world and the learned world in a loop: collect real data, train the world model, improve the policy in the model, then test against reality.
- Do not assume humanoid embodiment is required; task-specific machines with simpler control interfaces may be easier to learn and deploy.
- Track whether a model's benchmark success depends on narrow environment distribution.

## Open Questions

- Can action-labeled game data transfer broadly into physical robotics?
- Which architectures are most useful for planning: latent prediction, diffusion or flow-based generation, VLA-style foundation models, or hybrids?
- How much action can be inferred from video without ground-truth controls?
- What safety checks are needed when agents can act in real environments after training in synthetic ones?
- Which applications need full physical fidelity, and which only need "good enough" compressed prediction?

## Canonical Sources

- [[sources/ai-agents/Packy McCormick and Pim De Witte - World Models Computing the Uncomputable]]
- [[sources/ai-agents/Packy McCormick and Evan Beard - Many Small Steps for Robots]]
