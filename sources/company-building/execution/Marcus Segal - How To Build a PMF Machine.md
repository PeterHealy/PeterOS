---
type: source-summary
title: How To Build a PMF Machine
author: Marcus Segal
published: 2026-03-24
ingested: 2026-05-07
status: processed
url: https://speedrun.substack.com/p/how-to-build-a-pmf-machine
summary_basis: full source plus user-provided excerpts
raw_source: "[[raw/company-building/execution/marcus-segal-how-to-build-a-pmf-machine-highlight-capture]]"
tags:
  - company-building
  - execution
  - product
  - pmf
  - roadmapping
  - metrics
---

# How To Build a PMF Machine

## Summary Basis

- URL: <https://speedrun.substack.com/p/how-to-build-a-pmf-machine>
- Based on: full Substack article, accessible during ingest
- Raw capture: [[raw/company-building/execution/marcus-segal-how-to-build-a-pmf-machine-highlight-capture]]

## What This Source Is

A guest post in a16z speedrun by investor Marcus Segal about using roadmapping discipline to find and keep product-market fit. The article draws on Segal's experience at Zynga, as a founder, and as a startup mentor and investor.

For this wiki, the useful part is the operating system: define the metric before building, externalize feature ideas, rank them by expected impact, estimate effort, and review shipped work on a tight cadence.

## Source Summary

Segal argues that product-market fit is not a mystical one-time arrival. Founders can improve their odds by building a repeatable machine for generating hypotheses, shipping, measuring, and reallocating engineering time toward what works.

The article opens from a founder-resource frame. The CEO's job is to avoid running out of money before finding PMF. Engineering hours are the company's most valuable scarce resource. Because of that scarcity, PMF is more likely when the team uses an explicit roadmapping process rather than building whatever feels urgent.

Zynga is the central example. Segal says Zynga did not initially know how to make great games, but it built a system for finding what worked quickly. The company shipped far more updates than competitors, tested many hypotheses, and redirected large cross-functional teams toward anything that showed promise. AI now changes the volume and speed of iteration, but it does not remove the need for prioritization.

The recommended process starts with a metric. Before building a feature, the team should state the customer value and the target metric in one sentence. The exact metric may vary across reach, retention, revenue, or another product outcome, but the discipline is mandatory because otherwise the team cannot judge whether the feature worked.

Next, all feature ideas should be written down and stack-ranked by their probability of moving the chosen metric. This prevents individual builders from carrying private feature lists and choosing work based on urgency, taste, or recency. The team then gives each item a rough effort estimate. Segal emphasizes that AI-assisted coding has weakened old intuition about effort: some formerly hard work is fast, while apparently simple polish, coordination, merging, and UI integration can still take much longer than expected.

After impact ranking and effort sizing, the roadmap is power-ranked by impact-to-effort. High-impact, low-effort items go first. Low-impact, high-effort items may never be worth doing. The roadmap then runs on a tight review cadence: look one week back and one week forward, compare expected versus actual metric movement, scrap MVPs that do not perform, and course-correct before engineering time is wasted.

The article closes with a cultural point. Teams should measure everything and reward calibrated prediction. If someone builds or proposes a feature and correctly predicts its effect, celebrate it. If the prediction is wrong, the point is not blame; the point is better calibration next time.

## Key Ideas

- PMF should be treated as a journey managed by process, not a destination passively waited for.
- Engineering time remains the scarce company resource even when AI makes code generation faster.
- Every feature should start with a sentence connecting customer value to a target metric.
- Private feature lists create coordination failure; ideas should be externalized and ranked as a team.
- AI coding changes effort estimation because code generation is not the same as finished product integration.
- Impact-to-effort ranking is a forcing function against expensive low-probability work.
- A one-week-back, one-week-forward roadmap cadence keeps learning fast enough for AI-era product iteration.
- Measurement should improve team calibration rather than create punishment for failed experiments.

## Your Captures

Exact user-submitted excerpts are preserved in [[raw/company-building/execution/marcus-segal-how-to-build-a-pmf-machine-highlight-capture]].

Selected exact capture anchors:

- "A CEO’s job is to not run out of money before finding PMF"
- "Engineering person hours are the most important resource in your company"
- "Finding and keeping PMF is more likely to occur with a roadmapping process"
- "Start with the metric, then build the feature."
- "Get all the ideas out, then stack rank them."
- "Power rank by impact-to-effort."

## Capture-Based Synthesis

- The strongest reusable idea is that roadmapping is not administrative overhead. It is a capital-allocation system for scarce engineering hours.
- The metric-first sentence is a useful guardrail against building for vibes: "We will launch Product X feature to give Y value to the customer moving Z metric."
- Impact-to-effort ranking should happen after all ideas are made visible. Otherwise the team is not prioritizing the real option set; it is prioritizing whoever's idea surfaced first.
- The cultural standard is prediction quality, not merely shipping velocity. Teams should get better at saying what they expect a feature to do before they build it.

## What Changed In The Wiki

- Added the raw user-submitted capture under `raw/company-building/execution/`.
- Added a reusable reference page at [[reference/company-building/execution/PMF Roadmapping Loop]].
- Linked the source from company-building execution and knowledge indexes.

## Claims Worth Tracking

- AI-assisted development makes product teams faster, but may also make coordination, polish, and UI integration harder to estimate.
- A short roadmap review cadence may be better than longer planning horizons for AI-era product teams.
- Teams that measure predictions and outcomes without punishing misses should calibrate faster than teams that only reward shipping.

## Caveats

- The article is written for founders and early product teams; later-stage product organizations may need more governance, dependencies, and customer segmentation than the compact loop describes.
- Metric-first discipline can still fail if the chosen metric is a bad proxy for user value.
- Zynga-style rapid testing works best in products where user behavior can be observed quickly and experimentation cost is low.
- The article argues for measurement, but it should be read alongside metric-failure cautions such as [[sources/reading-writing/blogs-essays-articles/Derek Thompson - How Metrics Make Us Miserable]].

## Related Pages

- [[reference/company-building/execution/PMF Roadmapping Loop]]
- [[reference/company-building/execution/Self-Imposed Accountability Board]]
- [[sources/company-building/execution/Nate Martins - Reluctantly Influential]]
- [[sources/reading-writing/blogs-essays-articles/Derek Thompson - How Metrics Make Us Miserable]]
- [[knowledge/company-building/README]]
