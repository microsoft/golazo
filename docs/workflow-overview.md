# Workflow & Board Anatomy

> Public draft – adapted from legacy Task Board section.

## Summary

The board (physical or digital) is the single shared model of current work. It makes flow,
bottlenecks, priorities, and collaboration needs obvious at a glance.

## Board Concept

Each ticket advances left → right through clearly defined stages (columns). Horizontal lanes (rails)
categorize urgency or work type. A healthy board lets any observer answer: What’s most urgent?
What’s blocked? Who needs help next?

## Columns (Lifecycle Stages)

Columns reflect state changes in learning and validation—not just coding steps. Suggested baseline:

1. **Backlog** – Candidate items with potential value but not yet committed. Anyone can propose.
   Acceptance criteria not guaranteed complete.
2. **Ready** – Highest‑priority, well‑understood items with clear acceptance criteria and initial
   sizing. Pull from here when you start new work.
3. **Analyze** – Shepherd prepares or updates a lightweight design doc, confirms assumptions, and
   obtains ≥2 peer signoffs.
4. **Engineer** – Implementation + tests + instrumentation. Peer reviews (≥2) required before moving
   forward.
5. **Release** – Code merges/deploys; feature flags or incremental rollout if applicable.
   Monitoring/observability verified.
6. **Customer Validation** – Stakeholder / user confirms value delivered or provides immediate
   feedback loop.
7. **Done** – Definition of Done fully met; learnings & any metrics captured for retrospective.

Teams may add a short "QA" or "Staging" column only if that validation cannot practically happen
inside Engineer or Release; avoid fragmenting the flow.

## Rails (Priority / Work Type Lanes)

Rails (aka swimlanes) categorize tickets by urgency or intent without mixing them visually.

- **Swarm** – Highest priority customer‑impacting issues. The team stops and collaborates. Target
  turnaround typically < 24 business hours.
- **Interrupt** – Unexpected but important asks (e.g., compliance request, executive demo). Limit
  active count (often 1) to protect focus.
- **Planned** – The steady value stream of intentionally prioritized work. Most capacity should live
  here.

Optional rails (use sparingly):

- **OOF / Time Off** – Visualize availability, not work.
- **Tracking** – Items mostly waiting on external parties. Use retrospectives to reduce reliance on
  this lane—it can hide flow debt.
- **Lead / Manager** – Long‑tail tasks owned by roles with fragmented time; isolates their slower
  cadence from standard WIP metrics.

## Flow Example

1. Backlog item is refined during planning; moves to Ready.
2. Engineer pulls it into Analyze, drafts design doc, gets two signoffs.
3. Moves to Engineer; implementation + tests + two PR reviews.
4. Deployed under Release; monitoring shows healthy.
5. Customer validates; feedback minor → Done.

```
Backlog → Ready → Analyze → Engineer → Release → Customer Validation → Done
```

## Backward Movement Policy

Tickets should almost never move left. When they do (e.g., from Release back to Engineer due to a
defect) the team records it and reviews the root cause in the next retrospective—treat it as an
optimization signal, not blame.

## Visual Cues (Recommended)

- Distinct tag or color per major workstream.
- Icons/labels for blocked items (e.g., ⛔) with short reason in description.
- Avatars or initials for active collaborators beyond the Shepherd.

## Related

- WIP & Flow → `wip-and-flow.md`
- Tickets → `tickets.md`
- Planning → `planning-and-prioritization.md`
