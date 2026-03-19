# Meetings

## Summary

Golazo keeps the list of meetings intentionally small. Each meeting should have a clear operational
reason to exist: unblock work, inspect the system, or adjust priorities. A meeting that only repeats
what is already visible on the board is usually a sign that the format needs work.

## Standup (Daily - 10 to 15 min)

Standup is run by ticket rather than by person. The team walks the board from right to left and from
highest-urgency rail to lowest.

For each active ticket, the shepherd should be able to answer:

1. What is needed to move the ticket forward?
2. Are there blockers or risks?
3. Is there any learning the team should know now?

After active tickets are discussed, available capacity should go first to Swarm work, then to
Interrupts, then to helping finish work already in flight before starting something new.

The coach should interrupt gently when the conversation drifts into:

- individual status recitation
- work being picked up out of priority order
- design debates that need a smaller follow-up conversation

## Retrospective (Every 1 to 2 weeks - 30 to 60 min)

The retrospective exists to inspect the system and choose improvements. It should not become a vague
complaint session or a ritual celebration detached from the actual work.

Suggested agenda:

1. Review what went well.
2. Review action items from the previous retrospective.
3. Inspect recent ticket data and notable outliers.
4. Choose specific changes or experiments.

### Value Stream Mapping

One useful practice is to examine the ticket that exceeded expectations most significantly. Before
the meeting, the coach identifies the ticket and the shepherd reconstructs a simple timeline.

During the discussion, the team should assume good intent and look for system causes: unclear scope,
dependency waiting, late review, excessive multitasking, missing validation, or similar patterns.
The point is to identify preventable delay, not to litigate personal performance.

## Planning Session (Every 1 to 2 weeks - 30 to 60 min)

Some teams combine planning with the retrospective to avoid creating another meeting block. That is
reasonable if both discussions still have enough focus.

During planning, the team should:

- review backlog items that are likely to matter soon
- clarify acceptance criteria and assumptions
- estimate effort, cost of delay, and business value
- reorder the top of the backlog

After planning, the coach moves the highest-priority items into Ready.

### Estimation Dimensions

Golazo often uses
[Weighted Shortest Job First (WSJF)](https://www.bing.com/search?q=weighted%20shortest%20job%20first)
for prioritization.

The idea is simple:

1. Estimate the cost of waiting.
2. Estimate the value of delivery.
3. Divide that by the effort required.

The common formula is:

```
WSJF = (Cost of Delay + Business Value) / Effort
```

Teams often use Fibonacci values as a relative scale for each dimension.

| Dimension      | Question                           | Guidance                                                    |
| -------------- | ---------------------------------- | ----------------------------------------------------------- |
| Effort         | How much focused engineering time? | Use a relative scale. Ideal days or complexity both work.   |
| Cost of Delay  | How painful is waiting?            | Consider deadlines, exposure, opportunity cost, or risk.    |
| Business Value | How much value arrives if we ship? | Consider customer impact, strategy, revenue, or efficiency. |

Higher WSJF scores suggest higher priority. That is directionally useful, but not precise.

### Example

| Ticket                          | Effort | Cost of Delay | Business Value | WSJF | Order |
| ------------------------------- | ------ | ------------- | -------------- | ---- | ----- |
| A: Expiring auth token rotation | 3      | 21            | 8              | 9.7  | 1     |
| B: New usage dashboard slice    | 5      | 8             | 13             | 4.2  | 2     |
| C: Refactor shared util         | 8      | 3             | 5              | 1.0  | 3     |

This model is useful because it makes tradeoffs explicit. It should not be mistaken for a precise
economic forecast.

### Facilitation Tips

- Estimate silently first to reduce anchoring bias
- Discuss the widest outliers rather than every number
- Capture assumption differences when they explain disagreement
- Re-estimate only when something material changes
- Keep only the top of the backlog tightly ordered

### Anti‑Patterns

- Manipulating estimates to force a preferred outcome
- Trying to size tickets that are obviously too large
- Keeping stale backlog items indefinitely
- Treating WSJF as objective truth
- Avoiding cost-of-delay discussion because it is imperfect

### After Planning

- The coach moves the next set of items into Ready
- Tickets may be updated with links to notes or recordings if that helps later review
- Promising but deferred ideas should stay visible without cluttering the near-term backlog
- On some teams, business value and cost of delay are better filled in by a smaller group after the
  meeting if the broader team lacks the right context

### Tooling

Teams using Azure DevOps may find the
[Estimate](https://marketplace.visualstudio.com/items?itemName=ms-devlabs.estimate) extension useful
for planning and bulk editing.

## Starfish Retrospective (Quarterly)

This is a broader health check that asks the team to categorize observations under Start Doing, Stop
Doing, Keep Doing, Do More, and Do Less. Inputs are usually collected privately, then clustered into
themes for discussion.

The format is useful when the team needs a wider lens than the normal ticket-by-ticket
retrospective.

## Meeting Anti‑Patterns

- Reciting status already visible on the board
- Running design debates inside standup
- Allowing standup to go silent when help is needed
- Carrying unresolved retrospective actions from cycle to cycle
- Arguing numbers in planning instead of clarifying assumptions
- Keeping meetings that the team no longer finds useful without inspecting why

## Navigation

[← Step 6: Design Docs](design-docs.md) | [Step 8: WIP & Flow →](wip-and-flow.md)
