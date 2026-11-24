# Meetings

## Summary

Use meetings to unblock tickets, decide what to improve, or reorder upcoming work. If the team only
reads out what's already on the board, change the format.

## Standup (Daily - 10 to 15 min)

Walk the board by ticket, from right to left and from the most urgent rail to the least urgent.

For each active ticket, the shepherd should be able to answer:

1. What is needed to move the ticket forward?
2. Are there blockers or risks?
3. What have you learned that the team needs to know now?

Once you've discussed the active tickets, put any spare time toward Swarm work first, then
Interrupts. Help finish work already in progress before starting something new.

The coach should interrupt gently when the conversation drifts into:

- personal status updates that don't help move a ticket
- work being picked up out of priority order
- design debates that need a smaller follow-up conversation

## Retrospective (Every 1 to 2 weeks - 30 to 60 min)

Use recent tickets to see what helped and what slowed the team down. Pick something to change.

Suggested agenda:

1. Review what went well.
2. Review action items from the previous retrospective.
3. Inspect recent ticket data and notable outliers.
4. Choose specific changes or experiments.

### Value Stream Mapping

Before the meeting, the coach picks the ticket that ran furthest past its estimate. The shepherd
writes down when it moved and when it waited.

Look for delays the team can prevent next time. Was the scope unclear? Did the ticket wait on
another team or sit in review? Focus on what happened without blaming the shepherd.

## Planning Session (Every 1 to 2 weeks - 30 to 60 min)

You can hold planning and the retrospective together if there's enough time for both.

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

1. Estimate the cost of waiting.
2. Estimate the value of delivery.
3. Add those estimates and divide by the effort required.

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

Start with higher-scoring tickets, then check whether the order makes sense.

### Example

| Ticket                          | Effort | Cost of Delay | Business Value | WSJF | Order |
| ------------------------------- | ------ | ------------- | -------------- | ---- | ----- |
| A: Expiring auth token rotation | 3      | 21            | 8              | 9.7  | 1     |
| B: New usage dashboard slice    | 5      | 8             | 13             | 4.2  | 2     |
| C: Refactor shared util         | 8      | 3             | 5              | 1.0  | 3     |

In this example, the expiring token ranks first because waiting is costly and the fix is smaller.

### Facilitation Tips

- Estimate silently first to reduce anchoring bias
- Discuss the widest outliers rather than every number
- Write down which assumptions led to different estimates
- Estimate again only when a change could affect the result
- Keep only the top of the backlog tightly ordered

### Anti‑Patterns

- Manipulating estimates to force a preferred outcome
- Trying to size tickets that are obviously too large
- Keeping stale backlog items indefinitely
- Letting the score settle a disagreement without discussing the estimates
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

Use it to discuss habits that affect more than one ticket, such as how the team hands off reviews.

## Meeting Anti‑Patterns

- Reciting status already visible on the board
- Running design debates inside standup
- Allowing standup to go silent when help is needed
- Carrying unresolved retrospective actions from cycle to cycle
- Arguing numbers in planning instead of clarifying assumptions
- Keeping meetings that the team no longer finds useful without inspecting why

## Navigation

[← Step 6: Design Docs](design-docs.md) | [Step 8: WIP & Flow →](wip-and-flow.md)
