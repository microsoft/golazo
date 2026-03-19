# Adopting Golazo

## Summary

Golazo is easiest to evaluate through a deliberate trial rather than through partial adoption. Teams
that keep the visible parts while skipping the harder coordination practices usually conclude that
the method provides little value. In most cases, that is an observation about the partial adoption,
not about the full system.

A 90-day trial is usually long enough to give an idea about the strengths and explore the friction.

## Team Size and Suitability

Golazo tends to fit best for teams with roughly 6 to 8 engineers, though smaller teams can often use
it effectively and larger teams can split into multiple boards with explicit coordination.

Research-heavy or platform-heavy teams may need to adapt how they define tickets, but they should
still preserve short validation cycles where possible. If the work routinely takes too long to
validate, the rest of the process gets weaker.

## Prerequisites

| Area                 | Requirement                                                       | Notes                              |
| -------------------- | ----------------------------------------------------------------- | ---------------------------------- |
| Leadership Support   | Agreement not to override core practices mid-trial                | Prevents early erosion             |
| Coach                | Access to an experienced coach for at least the first 4 weeks     | Internal or borrowed is fine       |
| Tooling              | Visual board, design doc space, and shared communication channels | Keep tooling lightweight           |
| Psychological Safety | Retrospectives must be safe enough for honest discussion          | Otherwise the feedback loop breaks |

## Handling Downsides and Concerns

| Concern                                | Response                                                                                                            |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| "Too much ceremony"                    | Measure the actual time spent. The overhead should be small relative to the rework it prevents.                     |
| "Hard boundary with other teams"       | Use the Ready gate and early design sharing to coordinate dependencies rather than relying on informal handoffs.    |
| Career progression for senior IC scope | Senior engineers still lead through shaping, review, architectural guidance, and mentoring.                         |
| "Design docs slow us down"             | They add a small upfront cost, but many teams find the total delivery time falls because late-stage churn is lower. |

These concerns are legitimate. They should be tested against actual team experience, not dismissed.

## Common Anti‑Patterns

- Adopting standup or the board while skipping design docs or review discipline
- Ignoring WIP limits when pressure increases
- Turning spikes into hidden implementation work
- Treating customer validation as optional once the code is merged
- Customizing the board too early, especially by adding more states before the baseline is stable

## Adoption Checklist

- [ ] Board created with columns, rails, and WIP limits
- [ ] Communication channels available and in active use
- [ ] Design doc template easy to find
- [ ] First 10 backlog items refined and prioritized
- [ ] On-call engineer playbook drafted
- [ ] Meetings scheduled

## Navigation

[← Step 9: Communication](communication.md) | [Step 11: FAQ →](faq.md)
