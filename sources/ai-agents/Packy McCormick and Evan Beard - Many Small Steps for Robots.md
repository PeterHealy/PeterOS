---
type: source-summary
title: "Packy McCormick and Evan Beard - Many Small Steps for Robots, One Giant Leap for Mankind"
author: Packy McCormick and Evan Beard
published: 2026-01-16
ingested: 2026-05-07
status: processed
url: https://www.notboring.co/p/robot-steps
summary_basis: full source URL plus user-provided excerpts
raw_source: "[[raw/ai-agents/not-boring-robot-steps-highlight-capture]]"
tags:
  - ai-agents
  - robotics
  - embodied-ai
  - robot-data
  - company-building
---

# Packy McCormick and Evan Beard - Many Small Steps for Robots, One Giant Leap for Mankind

## Summary Basis

- URL: https://www.notboring.co/p/robot-steps
- Based on: full source URL, read on 2026-05-07, plus the user's submitted excerpts.
- Raw capture: [[raw/ai-agents/not-boring-robot-steps-highlight-capture]]

## What This Source Is

A Not Boring essay co-written by Packy McCormick and Evan Beard, co-founder and CEO of [[reference/Tools And Websites|Standard Bots]]. The essay argues against the "giant leap" view of robotics and for a deployment-led strategy: automate valuable constrained tasks today, collect robot-specific data from real failures, and climb the gradient of real-world variability one use case at a time.

## Source Summary

The article opens by contrasting two robotics strategies. The "Giant Leap" view says robotics value will unlock when models, compute, and data cross a threshold that produces general robots able to walk into almost any environment and work. Beard's "small steps" view says economically valuable work sits on a spectrum between fixed motion replay and fully general autonomy, and that most value will be captured by moving across that spectrum incrementally.

The core organizing concept is variability: the range of tasks, environments, objects, edge cases, humans, instructions, and recovery conditions a robot must handle. Low-variability automation already supports large industrial robotics businesses, despite brittle programming and expensive integration. Standard Bots' thesis is that AI-native robots can expand the addressable slice of this spectrum before general physical intelligence exists.

The data argument is the center of the essay. Robotics is unlike LLMs because there is no internet-scale corpus of aligned embodied action data. Architectures such as diffusion policies, VLAs, action chunking, and robot foundation models are useful, but they still need examples of the specific robot, task, environment, sensors, end effector, forces, and edge cases involved. Robots can interpolate inside their training distribution; they struggle when the physical situation moves outside it.

The essay is skeptical of ordinary video as a complete substitute for embodied robot data. Video can teach trajectories, sequencing, affordances, goals, timing, rhythm, grasp order, and some tool-use cues. But it does not directly contain mass, force, compliance, friction, stiffness, contact dynamics, torque, or the felt feedback of interaction. Humans infer some of that because they have lifelong embodied priors; robots do not. That is the embodiment gap.

Simulation and world models get similar treatment. The authors acknowledge that simulation can be powerful for rigid-body dynamics and that world models are directionally important, but argue that industrial reality contains too much hidden contact detail, deformability, sensor mismatch, and task-specific messiness for simulation alone to remove the need for real deployment data.

The proposed business strategy is to get paid to collect the necessary data. Standard Bots deploys industrial arms into customer environments, handles the first useful version of a task, teleoperates or intervenes when failures occur, and turns those interventions into training data. Failure-region data is especially valuable because it shows exactly where the robot's state distribution diverges from the model's expectations.

The cow-temperature example illustrates two lessons. First, customers reveal jobs founders would not have guessed from first principles. Second, many valuable robot tasks are not humanoid-shaped. A stationary, task-specific system with the right gripper, sensors, control loop, and model may be both cheaper and more capable than a humanoid for a constrained job. The piece extends this into a broader critique of humanoid ROI in factories, warehouses, farms, and homes.

Vertical integration is presented as both a technical and strategic requirement. The authors argue that robot data is far more efficient when aligned with the exact hardware that will deploy the policy. Controlling the arm, torque sensing, firmware, data collection, model training, and customer feedback loop lets Standard Bots adapt the whole system when new edge cases appear. Old motion-replay robots lack the real-time torque control and sensing needed for AI-controlled interaction.

The model-size argument is pragmatic. Large general models are tempting, but parameter count scales with variability, not economic value. Many industrial tasks can be solved by smaller distilled or fine-tuned models when the task is valuable, the variability is bounded, and the right data is available. For robotics, small models with the right embodied data can be faster, cheaper, easier to debug, and more useful than giant general models.

The essay closes by reframing the Bitter Lesson for robotics. Compute matters, but compute only dominates when the training data exists. Tesla's scale advantage in self-driving came from distribution and deployment, not from waiting in the lab. Beard's version of the lesson is that real-world robot deployment is how companies collect the data that lets scaling methods work.

## Key Ideas

- Robotics progress is not gated by one architectural breakthrough; it is constrained by the gradient of real-world variability.
- Useful robotics sits between deterministic automation and full autonomy, not only at either extreme.
- Robot data needs diversity, on-policyness, curriculum, and hardware alignment.
- Video is useful pretraining, but it misses forces, friction, stiffness, compliance, torque, and contact dynamics.
- Demonstration and teleoperation are high-bandwidth ways to transfer intent for physical tasks.
- Failure interventions are especially valuable training data because they concentrate on the boundary where autonomy breaks.
- Customers are a use-case discovery engine; they reveal valuable jobs founders would not imagine.
- Humanoid form factors can be both overkill and underkill for specific industrial or agricultural jobs.
- Vertical integration is useful while the market is still in the product-innovation phase and hardware, data, and models need to co-evolve.
- Smaller task-specific models can outperform large general models when value is concentrated in constrained work.

## Your Captures

Exact user-submitted excerpts are preserved in [[raw/ai-agents/not-boring-robot-steps-highlight-capture]]. No explicit PNote annotations were included.

Selected capture themes:

- Video carries trajectories, sequencing, affordances, goals, timing, rhythm, grasp order, and some tool-use cues.
- Video does not carry mass, force, compliance, friction, stiffness, or contact dynamics.
- The embodiment gap is the difference between seeing what to do and feeling what it is like to do it.
- The cow-temperature example shows customer-led use-case discovery and why humanoids are often the wrong default.

## Capture-Based Synthesis

- The submitted excerpts emphasize the data-quality gap between visual imitation and embodied control. This is a useful correction to "train on YouTube" robotics optimism.
- The cow example is not mainly about the oddity of the task. It is a compact market-discovery lesson: high-value automation opportunities are often hidden in repetitive, unpleasant, operationally specific jobs.
- The humanoid critique is strongest when framed as job-to-machine fit, not as a claim that humanoids will never matter. For many constrained jobs, the right sensor and actuator stack matters more than human resemblance.
- The most reusable company-building lesson is "get paid to collect the hard data." Deployment is not a distraction from model improvement; for physical AI, it may be the only scalable path to the right data.

## Claims Worth Tracking

- Robot-specific data may be 100x to 1,000x more efficient when aligned with the exact deployment hardware.
- Intervention data near failures may be more useful than broad sampling of cases the robot already handles.
- Most economically valuable industrial robotics tasks may be solvable by smaller task-specific models rather than giant general models.
- The robotics industry may remain vertically integrated until enough use cases and interfaces stabilize for modular suppliers to win.
- Humanoid robots may struggle to justify ROI in factories, warehouses, farms, and homes until reliability and safety become much higher.
- Foundation-model robotics companies may commoditize models, leaving customer relationships and deployment data as the durable moat.

## Caveats

- The article is co-written with the CEO of Standard Bots, so it is both a robotics argument and a company thesis.
- The Standard Bots revenue, deployment, pipeline, model, and hardware claims should be independently verified before being used as investment facts.
- The article argues from industrial robotics experience; some claims may transfer poorly to home robotics, autonomous vehicles, or domains with different data-collection economics.
- The humanoid critique is strongest for near-term ROI and task fit, not as a proof that human-shaped robots can never become useful.

## What Changed In The Wiki

- Added [[knowledge/ai-agents/Robotics Data And Deployment Gradient]] as a durable page for the deployment-led robotics thesis.
- Updated [[knowledge/ai-agents/World Models]] with this source as a related robotics-data counterweight.
- Updated [[reference/Tools And Websites]] with reusable robotics companies and resources mentioned in the source.

## Open Questions

- Which robotics tasks have enough economic value and bounded variability to justify early deployment before high reliability?
- How should a robotics company decide when to use teleoperation, direct manipulation, simulation, human video, robot self-play, or customer interventions?
- Where do humanoids have genuine form-factor advantage rather than demo advantage?
- How much real-world deployment data is needed before robot foundation models generalize across adjacent industrial use cases?
- Does vertical integration remain a durable moat, or does it become a temporary requirement before robotics modularizes?

## Related Pages

- [[knowledge/ai-agents/Robotics Data And Deployment Gradient]]
- [[knowledge/ai-agents/World Models]]
- [[reference/Tools And Websites]]
- [[raw/ai-agents/not-boring-robot-steps-highlight-capture]]
