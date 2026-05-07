---
type: reference
title: PMF Roadmapping Loop
status: active
created: 2026-05-07
updated: 2026-05-07
tags:
  - company-building
  - execution
  - product
  - pmf
  - roadmapping
  - metrics
---

# PMF Roadmapping Loop

## What It Is

A lightweight operating cadence for finding and keeping product-market fit by allocating engineering time toward the features most likely to move a chosen metric.

The loop is useful when a small team can ship quickly but risks building an undisciplined pile of features.

## Core Principle

Start with the metric, then build the feature.

Use this sentence before committing engineering time:

```text
We will launch [feature] to give [customer segment] [specific value], moving [metric].
```

If the sentence cannot be written clearly, the feature is not ready for the roadmap.

## Weekly Loop

1. Choose the current target metric.
2. Write down every feature, experiment, fix, or product idea.
3. Rank each idea by probability of moving the target metric.
4. Estimate rough effort for each idea.
5. Power-rank by impact-to-effort.
6. Ship the highest-ranking work.
7. One week later, compare expected versus actual metric movement.
8. Keep, deepen, revise, or scrap the work based on what happened.
9. Calibrate the team by recording which predictions were accurate.

## Ranking Table

| Idea | Customer value | Target metric | Expected impact | Effort | Decision |
|---|---|---|---|---|---|
|  |  |  | High / Medium / Low | S / M / L / XL | Do now / Later / Maybe never |

## Review Questions

- What did we ship last week?
- What did we expect each shipped item to do?
- What actually happened?
- Which prediction was most accurate?
- Which prediction was wrong in an informative way?
- What should we do, stop, or change this week?

## Useful Guardrails

- Do not rank ideas that are only in someone's head.
- Do not accept "better UX" as the metric unless it has a concrete behavioral proxy.
- Do not treat AI-generated code volume as finished-product velocity.
- Do not punish wrong predictions when they were explicit and honestly reviewed.
- Do not keep polishing an MVP that failed to move the target metric unless there is a clear diagnosis.

## Failure Modes

- Choosing vanity metrics because they are easy to move.
- Switching metrics every week before the team can learn anything.
- Letting the loudest person define impact.
- Ignoring integration, QA, and polish effort because the first code draft was fast.
- Shipping without writing down the expected effect.

## Canonical Source

- [[sources/company-building/execution/Marcus Segal - How To Build a PMF Machine]]
- <https://speedrun.substack.com/p/how-to-build-a-pmf-machine>
