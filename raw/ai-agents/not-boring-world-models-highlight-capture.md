---
type: raw-source
title: Not Boring - World Models Highlight Capture
author: Packy McCormick and Pim De Witte
published: 2026-03-19
captured: 2026-05-07
source_type: article-highlight-submit
url: https://www.notboring.co/p/world-models
tags:
  - ai-agents
  - world-models
  - embodied-ai
  - robotics
  - games
---

# Not Boring - World Models Highlight Capture

Canonical source: https://www.notboring.co/p/world-models

Captured from a `[SUBMIT]` chat message on 2026-05-07.

No explicit `PNote` annotations were included in the submit.

## User-Pasted Capture

As humans, we imagine easily, whether it's complex sports stadiums, potential romance, or heated discussions. We don't have to work harder to imagine ourselves at the next Manchester United game than we do to imagine talking to a friend we've known for years, even though imagining a Manchester game includes simulating and modeling the behavior of thousands of people, something that would take years for traditional computers and game engines today1.

Think about writing the code to describe the Man U match: at any moment, a fan might bring a random, home-crafted flag. The entire stadium starts singing a song related to it. Only some will sing, though; others will jump with their kids, while an old couple sits still, wondering if this is their last game together, soaking in every second in silence.

The world is a place where unexpected futures unfold, but in somewhat predictable ways. As humans, we can envision almost all of them with roughly the same amount of effort with a very similar amount of time given to each thought. Computers can't.

_________________________________________

But predicting raw pixel worlds for everything can be expensive and often wasteful. Most of what's in a video frame doesn't change from one moment to the next; the walls stay where they are, the sky remains the sky. And most of the details within a frame are redundant; the color of the sky, the texture of a wall. They could be described in a more compact form.

So modern World Models involve a latent space: a compressed, learned representation where only the most essential information is retained.

The visual encoder compresses each frame down to a compact vector (a mathematical fingerprint of the scene) and the model learns to predict the next fingerprint - not every pixel in the 4K frame - in response to actions. This is where the computational efficiency comes from.

To accurately model the evolution of the world, World Models must also learn to represent the full set of possible outcomes. This uncertainty in outcomes is usually referred to as the stochasticity of the environment.

World Models have to learn to navigate what they don't know yet (epistemic uncertainty: for example, a model that has never seen a traffic light will not know that red follows after yellow) and the inherently unknowable (aleatoric uncertainty: the randomness, like rolling dice5).

Even when the model has learned all that's possible to know about the behavior of the environment (it has reduced its "epistemic" uncertainty to a minimum), there will almost always be some inherent uncertainty ("aleatoric" uncertainty) in what happens next. This is in contrast to pure entertainment video models, which only need to be able to predict a common evolution of the world state to perform well.

If you use a straightforward prediction approach (for example, a model naively trained with Mean Squared Error, or MSE) to predict a car turning a corner, the model can become 'blurry' because it averages every possible outcome. The car could turn and stay in the left lane, or it could merge into the right lane. The trajectory that actually minimizes the error is the implausible one where the car stays in the middle of the two lanes. That's the blurriness, and different models handle it differently.

_____________________________

Here is a key insight behind World Models: actions are the ultimate form of compression.

Consider what happens when you decide to step left to avoid a puddle. Your brain processes the visual scene (the sidewalk, the puddle, the people around you, the curb, the approaching bus), predicts the immediate future (the puddle won't move, the bus will pass, the person behind you will keep walking), evaluates options (step left, step right, jump, accept wet shoes), and selects one.

An outside observer can't see inside your head, can't know exactly what you were thinking, can't know what you're processing subconsciously. They don't know if you're tired or if you're in a rush. They don't know your moral code, how you, specifically, would answer the Trolley Problem. They don't need to. They see the output of all of that near-instantaneous calculation: step left.

That, to me, is magic.

Of course, not everyone makes the right decisions. Play the video forward and you are able to learn the consequences, too. Step left, into an even bigger puddle. Step left, and get clipped by a car. Step left, and knock a baby out of its stroller. Over billions and billions of observations and instructions and actions, we learn not just how humans decide to respond based on inputs, but the consequences of those decisions. The collective World Model learns to act smarter than any individual.

_______________________________________________
Games are fun, of course. But the reason games keep showing up is that games are the only domain where you get massive amounts of labeled spatial-temporal data with clear action-outcome pairs, consistent physics, unambiguous reward signals, and a controlled environment where you can run millions of experiments. The real world has none of these properties.
