# Adopting Golazo: 90‑Day Trial

> Public draft – integrates legacy FAQ transition guidance and downsides with a structured rollout.

## Summary

A deliberate 90‑day, "by the book" trial lets a team experience full benefits (flow, quality,
learning) before deciding what to tailor. Partial adoption early almost always underdelivers.

## Team Size and Suitability

Ideal core team size: 6–8 engineers (smaller works; larger may split into two boards with periodic
sync). Research‑heavy teams or platform teams can adapt ticket definitions but should maintain short
validation cycles.

## Prerequisites

| Area                 | Requirement                                                            | Notes                               |
| -------------------- | ---------------------------------------------------------------------- | ----------------------------------- |
| Leadership Support   | Agreement not to override core practices mid‑trial                     | Shield from premature customization |
| Coach                | Access to experienced internal/external coach (at least first 4 weeks) | Can be borrowed from another team   |
| Baseline Metrics     | Current incident rate, average ticket time, review latency             | Enables before/after comparison     |
| Tooling              | Visual board, shared design doc space, chat channels                   | Keep setup lightweight              |
| Psychological Safety | Blameless retros and VSM expectation                                   | Essential for honest improvement    |

## Phase 1 (Weeks 1–3): Learn and Prepare

Goals: establish shared vocabulary and instrumentation.

- Kickoff presentation (overview and Q&A).
- Stand up board with columns/rails and WIP limits.
- Seed backlog (enough refined tickets for 1–2 weeks).
- Create core channels (Dev General, Review, Release, Social).
- Run first Planning and Retro (even if thin).
- Draft first design docs (paired creation to teach template).
- Start capturing baseline metrics.

## Phase 2 (Weeks 4–8): Full Trial

Goals: stabilize flow and reinforce habits.

- Enforce WIP limits rigorously.
- Require design doc and 2 signoffs before engineering (except true Swarm).
- Weekly Retros (or bi‑weekly if stable) with action items.
- DRI rotation weekly; capture repetitive toil for automation proposals.
- Track cycle time, review latency, interrupt %.
- Encourage cross‑area ticket selection to broaden knowledge.

## Phase 3 (Weeks 9–12): Optimize and Decide

Goals: evaluate impact; identify _informed_ adaptations.

- Aggregate before/after metrics (cycle time, incident rate, morale pulse).
- Value Stream Map 1–2 outlier tickets.
- Run a Starfish Retro focusing on adoption experience.
- Decide: adopt fully, pivot, or run extended experiment for specific dimensions.
- Document any customizations with rationale and rollback criteria.

## Success Criteria (Examples)

| Dimension        | Indicator                                | Target Improvement              |
| ---------------- | ---------------------------------------- | ------------------------------- |
| Flow             | Median ticket cycle time                 | ↓ 20–30% vs baseline            |
| Quality          | % time on Swarm and Interrupt            | at most 30% (10% Swarm typical) |
| Learning         | % tickets with design doc and 2 signoffs | at least 95%                    |
| Knowledge Spread | Distinct Shepherds per workstream        | Trending upward                 |
| Morale           | Pulse survey: "I can get help quickly"   | at least 4/5 average            |

## Handling Downsides and Concerns

| Concern                              | Response                                                                                                                         |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| "Too much ceremony"                  | Ceremonies are intentionally short; measure time spent—should be a small fraction vs regained flow.                              |
| "Hard boundary with other teams"     | Use Ready gate and clear acceptance criteria to collaborate; share design docs early with dependents.                            |
| Career progression (senior IC scope) | Seniors lead architectural alignment, backlog shaping, mentoring—document leadership contributions in design rationale & retros. |
| "Design docs slow us down"           | Track PR churn before/after; most teams see net reduction in total time to deliver.                                              |

## Common Anti‑Patterns

- Cherry‑picking only “visible” practices (standup) while skipping design docs or reviews.
- Ignoring WIP limits when pressure rises (“just this once”).
- Letting spikes grow into hidden implementation work.
- Delaying customer validation—tickets linger in Release/Done without confirmation.
- Premature customization (adding extra columns) before baseline flow is stable.

## Adoption Checklist

- [ ] Board created with columns, rails, WIP limits
- [ ] Channels live & norms documented
- [ ] Design doc template accessible
- [ ] First 10 backlog items refined & prioritized
- [ ] Metrics instrumentation (manual spreadsheet acceptable initially)
- [ ] DRI runbook drafted
- [ ] Pulse survey questions defined

## Related

- Why Golazo → [Why Golazo](why-golazo.md)
- Measuring Success → [Measuring Success](measuring-success.md)
- Communication → [Communication Patterns](communication.md)
