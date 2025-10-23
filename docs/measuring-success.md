# Measuring Success & Health Metrics

> Public draft – synthesizes legacy Dashboard discussion + FAQ validation guidance.

## Summary

Healthy Golazo adoption shows up as shorter cycle times, stable quality, broad knowledge
distribution, and high morale. Use a lightweight mix of leading (predictive) and lagging (outcome)
indicators—never vanity metrics.

## Leading Metrics (Predict Flow Issues Early)

| Metric            | Definition                                             | Why It Matters                       | Target / Heuristic                                    |
| ----------------- | ------------------------------------------------------ | ------------------------------------ | ----------------------------------------------------- |
| Cycle Time        | Start → Done per ticket (median)                       | Measures flow speed                  | Trending downward / stable; large spikes investigated |
| WIP Age           | Elapsed time current tickets have spent in each column | Early warning of future delays       | Aging tickets trigger discussion in standup           |
| Review Latency    | Time from PR ready to first substantive review         | Signals collaboration responsiveness | Aim < 4 business hours median                         |
| Flow Efficiency   | (Active time)/(Total elapsed) estimate                 | Highlights waiting waste             | Increase by reducing handoff delays                   |
| Ready Queue Depth | Count of tickets in Ready                              | Prevents starvation / over‑stocking  | 1–2 weeks of work max                                 |

## Lagging Metrics (Validate Outcomes)

| Metric                  | Definition                              | Signal                               |
| ----------------------- | --------------------------------------- | ------------------------------------ |
| Incident Rate           | Number of production incidents / period | Quality & resilience trend           |
| Defect Escape           | Bugs found post‑release vs pre‑release  | Test & design effectiveness          |
| Interrupt %             | (Interrupt + Swarm time)/(Total)        | Operational noise; should trend down |
| Delivery Predictability | % tickets completed within SLA          | Sizing + flow discipline             |
| Knowledge Distribution  | Distinct Shepherds per workstream       | Avoids silos; should broaden         |
| Morale / Engagement     | Pulse survey composite                  | Sustainability of pace               |

## Qualitative Signals

- Stakeholder surprise decreases (fewer “I didn’t know you were doing that”).
- Retros include systemic improvements, not just tactical fixes.
- New hires independently shepherd a ticket within first few weeks.
- Reduced hallway (ad hoc) dependency clarifications—design docs answer them.

### Monthly Pulse Survey (Example – 1–5 scale)

1. I can get help quickly when I’m blocked.
2. Our process helps me focus on the highest value work.
3. I’m learning new areas or deepening expertise regularly.

Track trends, not single data points.

## Dashboard Essentials

Minimum viable dashboard (spreadsheet or simple queries is fine):

- Completed tickets list (with Start/End dates, rail, effort estimate, actual cycle time).
- Distribution chart: ticket cycle time buckets.
- Interrupt vs Planned time ratio.
- Aging WIP (tickets > threshold, e.g., 7 days) report.
- Swarm frequency & mean time to resolve.
- Design doc adherence (% tickets with required signoffs).

## Signs of Drift / Anti‑Patterns

| Symptom                      | Possible Cause                                   | Action                                                 |
| ---------------------------- | ------------------------------------------------ | ------------------------------------------------------ |
| Rising cycle time & WIP Age  | Overloaded columns; ignoring WIP limits          | Enforce limits; swarm oldest ticket                    |
| Many backward moves          | Incomplete analysis / unclear Definition of Done | Strengthen design doc checklist                        |
| Review latency increasing    | Reviewer overload / large PRs                    | Encourage smaller tickets; assign reviewers explicitly |
| High Interrupt % (>40%)      | Quality or stakeholder expectation gap           | Root cause incidents; tighten acceptance criteria      |
| Few Shepherds per workstream | Knowledge silo forming                           | Intentionally route next tickets to new people         |

## Continuous Improvement Loop

1. Collect metrics (automated if possible; otherwise quick manual capture).
2. Highlight notable changes / outliers for retro (no raw data dump).
3. Select 1–2 experiments (e.g., reduce Ready depth, stricter spike timeboxes).
4. Apply for a cycle; measure impact.
5. Keep what measurably helped; revert rest.

## How Do We Know It’s Working? (FAQ Summary)

Ask the team directly: Are you happier, learning, and shipping value predictably? Objective metrics
should corroborate subjective improvement. If not, treat the gap as a design problem—adjust
experiments, not the goal.

## Related

- Why Golazo → `why-golazo.md`
- WIP & Flow → `wip-and-flow.md`
- Adoption Guide → `adoption-guide.md`
