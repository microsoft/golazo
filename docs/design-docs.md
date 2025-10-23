# Design Docs: Lightweight Shared Context

> Public draft – adapted from legacy Design Documents section plus rationale from FAQ & Reasons.

## Summary

Short design docs align intent, surface risks early, and create durable knowledge. They replace
expensive late PR debates with quick, high‑quality implementation and review cycles.

## Purpose & Benefits

- **Shared Context Before Code** – Ensures reviewers agree on approach, preventing rework.
- **Higher Quality Implementation** – Edge cases & test strategy considered upfront.
- **Faster Reviews** – PR feedback focuses on details, not fundamental direction changes.
- **Knowledge Base** – Future maintainers (including new hires) can reconstruct why decisions were
  made.
- **Onboarding Accelerator** – New contributors read similar docs to ramp and confidently propose
  work.
- **Metrics & Predictability** – Early sizing + estimated completion date highlight mismatches in
  understanding.

## Minimal Template

Keep it lean—optimize for clarity, not prose. (Full copyable version: `templates.md`.)

1. Elevator Pitch (value, for whom, why now)
2. Definition of Done (quality & outcome bullets)
3. Customer / Consumer (validator role)
4. Dependencies & Assumptions
5. Design & Testing Approach (sketch / outline OK)
6. Task List (implementation, tests, monitoring, docs, rollout)
7. Estimated Completion (95% confidence date)
8. Signoffs (2 peers)
9. Implementation Notes (filled as work proceeds)

Aim for 5–10 minutes to draft for straightforward tickets; larger efforts may justify a richer
diagram.

## Signoff Process

- Draft ready when all sections above have initial content.
- Two peers review (ideally from different familiarity levels) and either approve or request
  clarifications.
- Questions resolved asynchronously or in a short huddle; doc updated to reflect any changes.
- Only after two signoffs does engineering begin (unless a time‑critical swarm demands
  parallelization—rare and deliberate).

## During Implementation

- Keep doc open; append key discoveries, changed assumptions, data sources.
- If a major pivot emerges (e.g., architectural change), pause and re‑review—treat it like a micro
  design revision.
- Mark any deferred follow‑ups explicitly ("Out of scope follow‑ups" list) instead of silently
  expanding scope.

## Common Pitfalls & Avoidance

| Pitfall                                  | Consequence                         | Mitigation                                         |
| ---------------------------------------- | ----------------------------------- | -------------------------------------------------- |
| Skipping docs for “small” changes        | Hidden coupling, repeated fixes     | Keep even smaller docs—maybe 5 bullet points       |
| Writing essays                           | Slow to author & review, goes stale | Favor bullet lists + diagrams over paragraphs      |
| Signoff theater (“LGTM” without reading) | False confidence                    | Rotate reviewers; ask clarifying questions         |
| Using doc as status log                  | Noise burying rationale             | Put day‑to‑day notes in ticket; keep doc strategic |
| Letting divergences accumulate           | PR surprises                        | Update doc immediately on direction changes        |

## Review Quality Checklist (for Signers)

- Does the Definition of Done capture validation + quality signals?
- Are major risks & dependencies acknowledged?
- Can one person reasonably finish this within the SLA?
- Is the test/monitoring approach explicit?
- Are follow‑up items clearly out of scope?

## Related

- Tickets → `tickets.md`
- Templates → `templates.md`
- Reviews (Communication) → `communication.md`
