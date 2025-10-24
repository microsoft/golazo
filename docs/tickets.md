# Tickets & Sizing

> Public draft – adapted from legacy Tickets section (fields & spike guidance).

## Summary

A ticket is the smallest independently valuable slice of work that a single person can shepherd from
idea to validated outcome within the team’s SLA (commonly < 2 weeks). Every ticket must produce
demonstrable business or user value—no "just refactor because" items without a clear benefit.

## Ticket Definition

Each ticket represents a cohesive change that, when complete, can be reviewed, released, and
validated. It includes clear acceptance criteria and a definition of done covering quality signals
(tests, monitoring, docs) so the team can support it afterward.

## Core Fields

| Field               | Purpose                                                     | Notes                                                 |
| ------------------- | ----------------------------------------------------------- | ----------------------------------------------------- |
| Title               | Crisp outcome phrased as value ("Enable X so Y")            | Avoid vague verbs ("improve", "handle stuff")         |
| Shepherd            | Primary facilitator ensuring flow & quality                 | Not required to do all implementation                 |
| Acceptance Criteria | Observable conditions proving value delivered               | Written before significant engineering starts         |
| Cost Estimate       | Effort assuming focused work (e.g., ideal days / Fibonacci) | Used to spot outliers, not to micromanage             |
| Start / End Dates   | Actual flow timing for metrics & retros                     | Set explicitly when leaving Ready / entering Done     |
| Tags / Color        | Group by workstream/domain                                  | Avoid over‑tagging; supports dashboard & WIP insights |
| Definition of Done  | Quality checklist (tests, docs, monitors)                   | Can be templated or global + ticket specifics         |

## Sizing Rules (Checklist)

All must be true:

- Delivers standalone value (stakeholder can validate it in isolation).
- Fits within SLA (< 2 weeks; many teams aim for 2–5 days).
- Acceptance criteria and DoD can be unambiguously verified.
- Quality built in (tests + observability planned up front).
- Minimal design complexity (excess ambiguity → consider spike).

If any item fails, break the ticket down _before_ starting.

## Spike Tickets

Use a spike when uncertainty prevents meaningful acceptance criteria (e.g., unfamiliar API, unclear
algorithm feasibility). Characteristics:

- Goal: answer specific, enumerated questions.
- Output: documented findings + follow‑on concrete tickets.
- Time‑boxed: small (often ≤ 2–3 days). If answers expand scope, create a new spike rather than
  sprawling.
- Closure: team reviews answers; confirms next steps.

Scope spikes tightly. "Research database options" is weak; "Compare 3 time‑series storage options
across ingest cost, retention, query latency; recommend one" is actionable.

## Anti‑Patterns

- Tickets as mini‑projects spanning multiple weeks.
- Vague titles ("Clean up code", "Handle edge cases").
- Silent carrying of side work not on the board.
- Large refactors without articulated value (performance, reliability, clarity).
- Spikes that implement code instead of answering questions.

## Healthy Behaviors

- Split early when you detect dual outcomes emerging.
- Pair frequently on risky or novel tickets—faster learning, fewer surprises.
- Reference prior design docs for similar areas to maintain consistency.

## Related

- Design Docs → [Design Docs](design-docs.md)
- Planning → [Planning & Prioritization](planning-and-prioritization.md)
- WIP & Flow → [WIP & Flow](wip-and-flow.md)
