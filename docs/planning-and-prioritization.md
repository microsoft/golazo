# Planning & WSJF Prioritization

> Public draft – adapted from legacy Planning section with facilitation enhancements.

## Summary

Frequent, lightweight planning keeps the backlog aligned with current value signals. Weighted
Shortest Job First (WSJF) prevents gut‑feel prioritization and exposes trade‑offs explicitly.

## Cadence

Every 1–2 weeks (often paired with retrospective). Keep it short by ensuring tickets arrive
pre‑groomed with draft acceptance criteria.

## Inputs

- Candidate tickets (clear problem + acceptance criteria draft).
- Updated metrics (interrupt load, incident trends, cycle time).
- Strategic / stakeholder inputs (new opportunities, deadlines).
- Deferred follow‑ups from retros or design docs.

## Estimation Dimensions

Use a normalized Fibonacci scale (1,2,3,5,8,13,21) across the _whole backlog_, not per session.

| Dimension      | Question                           | Guidance                                                     |
| -------------- | ---------------------------------- | ------------------------------------------------------------ |
| Effort         | How much focused engineering time? | Can represent ideal days or complexity proxy. Keep relative. |
| Cost of Delay  | How painful is waiting?            | Deadlines, risk exposure, expiring certs, opportunity cost.  |
| Business Value | How much value when delivered?     | Customer impact, revenue, strategic leverage.                |

Calibrate extremes first: identify a “1” and a “21” for each dimension, then place others relative
to them. Adjust periodically if distribution skews.

## WSJF Formula

```
WSJF = (Cost of Delay + Business Value) / Effort
```

Lower WSJF result = higher priority (more value per unit effort sooner). Some teams sort descending
by the _ratio_ depending on definition—be explicit and consistent.

## Example

| Ticket                          | Effort | Cost of Delay | Business Value | WSJF ( (CoD+BV)/Effort ) | Order |
| ------------------------------- | ------ | ------------- | -------------- | ------------------------ | ----- |
| A: Expiring auth token rotation | 3      | 21            | 8              | 9.7                      | 1     |
| B: New usage dashboard slice    | 5      | 8             | 13             | 4.2                      | 2     |
| C: Refactor shared util         | 8      | 3             | 5              | 1.0                      | 3     |

## Facilitation Tips

- Silent estimate first (avoid anchoring), then reveal.
- Discuss widest outliers; converge quickly.
- Capture assumption differences (they teach, not just decide numbers).
- Re‑estimate only when key knowledge changed—not because a week passed.
- Keep only the top of the backlog perfectly ordered; lower items can be approximate.

## Anti‑Patterns

- Gaming numbers to force a pet project upward.
- Huge tickets that resist relative sizing (split first).
- Carrying stale, never‑revisited items for months.
- Treating WSJF as absolute truth (it’s a heuristic—sanity check occasionally).
- Skipping Cost of Delay because it “feels subjective” (it’s the point!).

## After Planning

- Coach (or designated facilitator) moves top items into Ready.
- Communicate changes (summary message or changelog ticket).
- Track any deferred but promising ideas separately (idea backlog) to avoid noise.

## Related

- Tickets → `tickets.md`
- Measuring Success → `measuring-success.md`
- Adoption Guide → `adoption-guide.md`
