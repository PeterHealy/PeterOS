---
type: raw-source
title: "Not Boring - Many Small Steps for Robots, One Giant Leap for Mankind Highlight Capture"
author: Packy McCormick and Evan Beard
published: 2026-01-16
captured: 2026-05-07
source_type: article-highlight-capture
url: https://www.notboring.co/p/robot-steps
capture_status: user-submitted-excerpts
tags:
  - ai-agents
  - robotics
  - embodied-ai
  - robot-data
---

# Not Boring - Many Small Steps for Robots, One Giant Leap for Mankind Highlight Capture

## Source Metadata

- URL: https://www.notboring.co/p/robot-steps
- Article title: "Many Small Steps for Robots, One Giant Leap for Mankind"
- Publication: Not Boring
- Authors: Packy McCormick and Evan Beard
- Published: 2026-01-16
- Captured: 2026-05-07

## User-Submitted Capture

Videos are useful for many things:

Trajectories and sequencing: Video is great at showing the arc of motion and the order of steps in an action.

Affordances and goals: You watch someone turn a knob and you learn that knobs want to be turned. Switches want to be pressed.

Timing and rhythm: Timing matters for things like locomotion, assembly, or anything that’s basically choreography. Video carries timing.

If you’re learning to grasp, video can show you: reach → descend → close fingers → lift.

And it can show tool use: the tilt of a cup, the swing of a hammer, the way people “cheat” by sliding things instead of lifting them.

But there are whole categories of data that video simply doesn’t carry: mass, force, compliance, friction, stiffness, contact dynamics.

Humans can sometimes infer some of this visually, but only because we’re leaning on a lifetime of embodied experience. Robots don’t have that prior.
.....................

That’s the embodiment gap. Video tells you what to do, but not what it feels like to do it. You can watch someone moonwalk all day. You still won’t feel how the floor grips your shoe, how much pressure transfers to your toes, how to modulate tension without faceplanting.

And robots have it worse than humans. At least we have priors. Robots have sensors and math.
_________________________

I was telling Packy (and he made me include this) about one of our new salespeople’s first days. He’d received a lead from a farm that wanted to use our robots to take their cows’ temperatures. Unusual temperature is the earliest, cheapest signal that something is wrong with a cow.

Do you know how to take a cow’s temperature?

What you do is, you take a thermometer and you stick it in the cow’s anus. You do this once a week, once a month, or somewhere in between, depending on the stage of the cow’s life. There are 90 million cows in the United States. Based on the cycle time math (it takes about one minute per cow) that’s a thousand-robot opportunity.

Two things about that opportunity:

If you’d said, “Evan, if your life depended on it, give me a job that you could automate in the dairy industry,” I would have said milking cows. I’d never think of automating sticking a thermometer in a cow’s anus. That’s a job you learn about from customers.

This is not a job for a humanoid. Surprisingly few jobs are, when you think about it.

One reason it’s not a job for a humanoid is that a humanoid would be overkill. You’re paying for general capabilities (and legs) when what you need is one thing done over and over and over (in a stationary position). Another reason is that a humanoid would be underkill for that specific job: it wouldn’t be set up, neither physically nor in the model, for the specific job.

What you’d need is a flexible gripper, for one thing. But really, it all comes down to entry speed. You can’t just jam it in. The cows don’t like that. And how do you figure out the right entry speed? Every cow is different. Turns out, you need a camera trained on the cow’s face and a model trained on hundreds of cows’ facial reactions; the cow’s face tells you when to slow down (and this behavior should emerge automatically during end-to-end training without any hand-crafted prior). The model needs to be able to understand what to do with that specific sensor data instantly in order to tweak the arm’s speed and angle of attack quickly enough for the cow to let it in. And so on and so forth.

Another reason it’s not a job for a humanoid is that they’re going to be pretty expensive. Elon himself predicted that by 2040, there will be 10 billion humanoids, and they’ll cost $20-25,000 each. About half that cost comes from the legs, which are probably a liability on the farm. Lots of shit in which to slip.

Here’s one more huge reason it’s not a job for a humanoid. Humanoids don’t exist today.

Other than some toy demonstrations, humanoids just do not exist in the field today. Generally intelligent robots certainly do not exist in the field today.

______________________________________________________
