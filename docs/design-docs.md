# Design Docs

## Summary

Short design docs align intent, surface risks early, and create durable knowledge. They replace
expensive late PR debates with quick, high‑quality implementation and review cycles.

## Purpose and Benefits

- Shared Context Before Code: Ensures reviewers agree on approach, preventing rework.
- Higher Quality Implementation: Edge cases and test strategy considered upfront.
- Faster Reviews: PR feedback focuses on details, not fundamental direction changes.
- Knowledge Base: Future maintainers can reconstruct why decisions were made.
- Onboarding Accelerator: New contributors read similar docs to ramp and confidently propose work.
- Metrics and Predictability: Early sizing and estimated completion date highlight mismatches in
  understanding.

## Minimal Template

Keep it lean. Optimize for clarity, not prose. (Full copyable version: see
[Templates & Examples](templates.md).)

1. Elevator Pitch (value, for whom, why now)
2. Definition of Done (quality and outcome bullets)
3. Customer / Consumer (validator role)
4. Dependencies and Assumptions
5. Design and Testing Approach
6. Task List (implementation, tests, monitoring, docs, rollout)
7. Estimated Completion (95% confidence date)
8. Signoffs (2 peers)
9. Implementation Notes (filled as work proceeds)

## Signoff Process

- Draft ready when all sections above have initial content.
- Two peers review and either approve or request clarifications.
- Questions resolved asynchronously; doc updated to reflect any changes. Multiple rounds of updates
  may warrant a meeting to discuss.
- Only after two signoffs does engineering begin (unless a time‑critical swarm demands
  parallelization. This is rare and deliberate).

## During Implementation

- Keep doc open; append key discoveries, changed assumptions, data sources.
- If a major pivot emerges (e.g., architectural change), pause and re‑review. Treat it like a micro
  design revision.
- Mark any deferred follow‑ups explicitly instead of silently expanding scope.

## Common Pitfalls and Avoidance

| Pitfall                                  | Consequence                           | Mitigation                                      |
| ---------------------------------------- | ------------------------------------- | ----------------------------------------------- |
| Skipping docs for "small" changes        | Hidden coupling, repeated fixes       | Keep even smaller docs, perhaps 5 bullet points |
| Writing essays                           | Slow to author and review, goes stale | Favor bullet lists and diagrams over paragraphs |
| Signoff theater (“LGTM” without reading) | False confidence                      | Rotate reviewers; ask clarifying questions      |
| Letting divergences accumulate           | PR surprises                          | Update doc immediately on direction changes     |

## Reviewer Checklist

- Does the Definition of Done capture validation and quality signals?
- Are major risks and dependencies acknowledged?
- Does the planned design fit with the existing architecture?
- Are there existing tools or resources that the author is unaware of?
- Can one person reasonably finish this within the SLA?
- Is the test/monitoring approach explicit?
- Are follow‑up items clearly out of scope?

## Navigation

[← Step 5: Tickets](tickets.md) | [Step 7: Meetings →](meetings.md)
