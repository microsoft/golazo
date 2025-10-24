# Measuring Success & Health Metrics

> Public draft – scaffold created to satisfy cross-page links.

## Summary

Golazo success is measured through a blend of flow, quality, learning, and morale indicators.
Metrics inform improvement experiments; they are never used as blunt performance weapons.

## Core Quantitative Metrics

| Metric                 | What It Shows                                    | Collection Notes                                     |
| ---------------------- | ------------------------------------------------ | ---------------------------------------------------- |
| Cycle Time             | Speed from Ready to Done                         | Median & 75th percentile over last 4 weeks           |
| WIP Age                | Aging items risk and hidden delays               | Highlight tickets > 2x median cycle time             |
| Review Latency         | Time from PR ready to first substantive feedback | Separate design doc vs PR latency if tracked         |
| Interrupt %            | Reactive load (Swarm and Interrupt vs total)     | Target: Interrupt and Swarm at most ~30% of capacity |
| Defect / Incident Rate | Quality & stability                              | Track by severity category                           |
| Ticket Size Compliance | % tickets within SLA (< 2 weeks)                 | Outliers trigger sizing discussion                   |
| Shepherd Distribution  | Knowledge spread & ownership equity              | Distinct Shepherds per workstream trending upward    |

## Qualitative Signals

| Signal         | Healthy Indicator                          | Concern Indicator                                |
| -------------- | ------------------------------------------ | ------------------------------------------------ |
| Retro Energy   | Frequent wins + candid improvement ideas   | Defensive tone; blame language                   |
| Review Quality | Specific, constructive comments            | "LGTM" rubber stamps; late architectural debates |
| Onboarding     | First validated ticket in weeks not months | Long shadowing before contribution               |
| Collaboration  | Pairing/micro-swarming visible             | Individuals hoarding complex areas               |
| Morale Pulse   | "I can get help quickly" >= 4/5 average    | Drop below 3 sustained                           |

## Dashboards & Visualization

A lightweight dashboard (spreadsheet or simple queries) should show at least: cycle time trend,
review latency rolling average, aging tickets list, interrupt % weekly, incident count. Keep charts
minimal—opt for clarity over aesthetics.

## Using Metrics Ethically

- Always pair numbers with narrative context.
- Use trends, not single data points, to decide changes.
- Never compare individuals; optimize the system.
- Treat unexpected spikes as learning opportunities.

## Improvement Loop

1. Observe metric deltas or qualitative signals.
2. Form a hypothesis ("Reducing Ready overfill will lower cycle time variance").
3. Implement a lightweight experiment (change WIP limit, adjust design doc checklist).
4. Re-measure after a defined period.
5. Keep or roll back based on outcome.

## Related

- WIP and Flow - [WIP & Flow](wip-and-flow.md)
- Tickets and Sizing - [Tickets & Sizing](tickets.md)
- Why Golazo - [Why Golazo](why-golazo.md)
- Adoption Guide - [Adoption Guide](adoption-guide.md)

---

_Iterate this page as real team usage yields better leading indicators._
