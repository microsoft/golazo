# Meetings

## Summary

Golazo favors a minimal set of tightly focused meetings. Each exists to unblock flow, amplify
learning, or adapt priorities. It is a non-goal to recite status already visible on the board.

## Standup (Daily – 10–15 min)

Order: board right to left, top (Swarm) to bottom (Planned). Discussion is by _ticket_, not by
person.

For each in‑progress ticket the Shepherd answers:

1. What is needed to move it to the next column?
2. Any blockers or risks?
3. Critical learning worth sharing?

After discussing all active tickets, if anyone is idle, staff Swarms first, then Interrupts, and
then help finish work before starting new.

All team members (but especially the Coach) should speak up if they observe:

- Long design debates
- Standard status report content such as what I did yesterday
- Tickets being picked up out of order (swarms > interrupts > help existing tickets > planned)

## Retrospective (Every 1–2 weeks – 30-60 min)

Goal: celebrate wins and identify waste and choose improvement experiments.

Suggested Agenda:

1. Celebrate and list successes
2. Review Change notes from previous retro
3. Review ticket data from previous weeks. Look for categories of swarms, unexpectedly long tickets,
   tickets that moved backward or were thrown away, etc.
4. Suggest actionable changes or renewed focus on specific Golazo process points

### Value Stream Mapping

Prior to the retrospective meeting, the coach should identify the ticket where the actual time taken
for the ticket most exceeded the expected time. Prior to the meeting, the Shepherd can review what
was done each day on the ticket. During the meeting, the Shepherd narrates a neutral, day‑by‑day
timeline. Team treats Shepherd as _innocent_ and instead the team focuses on what they could have
done to help the ticket close on time.. Dicsussions often revolve around system factors such as
dependencies, multitasking, and unclear definition of done). The goal of the discussionare concrete
prevention ideas to help the team be more efficient in the future.

## Planning Session (Every 1–2 weeks – 30-60 min)

Many teams pair this meeting with retro to avoid having additional meetings on the calendar, but
that can vary depending on how long the team usually spends on the retro content.

During planning, the team should:

- Review unestimated backlog items.
- Clarify acceptance criteria and effort assumptions.
- Assign Effort, Cost of Delay, Business Value (Fibonacci scale) then compute WSJF.
- Reorder backlog (only top items need perfect ordering).
- Pull highest priority items into Ready (Coach gates quality).

A meeting recording preserves reasoning for future reference.

### Estimation Dimensions

The estimation process is based on the
[Weighted Shortest Job First (WSJF)](https://www.bing.com/search?q=weighted%20shortest%20job%20first)
method.

All estimates are given using the Fibonacci scale. For each of the dimensions below, teams calibrate
the extremes by finding a "1" (low) and "21" (high) for each dimension. Then other items are placed
relatively. Generally this is simply a matter of discussing the numbers for the new items, but
periodically it is necessary to recalibrate the whole list.

| Dimension      | Question                           | Guidance                                                     |
| -------------- | ---------------------------------- | ------------------------------------------------------------ |
| Effort         | How much focused engineering time? | Can represent ideal days or complexity proxy. Keep relative. |
| Cost of Delay  | How painful is waiting?            | Deadlines, risk exposure, expiring certs, opportunity cost.  |
| Business Value | How much value when delivered?     | Customer impact, revenue, strategic leverage.                |

Once the three numbers are collected for each ticket, they are plugged into the WSJF formula:

```
WSJF = (Cost of Delay + Business Value) / Effort
```

A Higher WSJF result means the ticket is higher priority. The goal is to focus on getting more value
per unit of effort sooner. The Coach will use this prioritization to determine which tickets to pull
in to the Ready column.

### Example

| Ticket                          | Effort | Cost of Delay | Business Value | WSJF | Order |
| ------------------------------- | ------ | ------------- | -------------- | ---- | ----- |
| A: Expiring auth token rotation | 3      | 21            | 8              | 9.7  | 1     |
| B: New usage dashboard slice    | 5      | 8             | 13             | 4.2  | 2     |
| C: Refactor shared util         | 8      | 3             | 5              | 1.0  | 3     |

### Facilitation Tips

- Silent estimate first to avoid anchoring and then reveal.
  [Planning poker](https://www.bing.com/search?q=planning%20poker) is a good way to achieve this.
- Discuss widest outliers when voting. Hear from the high and low estimate and then converge
  quickly.
- Capture assumption differences.
- Re‑estimate only when key knowledge changed.
- Keep only the top of the backlog perfectly ordered; lower items can be approximate.

### Anti‑Patterns

- Gaming numbers to force a pet project upward.
- Huge tickets that resist relative sizing. Split them first.
- Carrying stale, never‑revisited items for months.
- Treating WSJF as absolute truth. It’s a heuristic—sanity check occasionally.
- Skipping Cost of Delay because it “feels subjective”.

### After Planning

- Coach moves top items into Ready.
- Update tickets with a link to the planning meeting recording to easily review context in the
  future.
- Track any deferred but promising ideas separately in an idea backlog to avoid noise.
- On some teams, individual engineers may not have a lot of insight into Cost of Delay or Business
  Value. While it's helpful to share this context, teams may find it more efficient for the Coach to
  fill these values in after the meeting and share the results with the team. The time with the
  whole team can focus on the effort estimation.

### Tooling

Note that if teams are using Azure Dev Ops to run their Golazo process, this planning meeting can
benefit from using the
[Estimate](https://marketplace.visualstudio.com/items?itemName=ms-devlabs.estimate) tool and then
tickets can be bulk edited for WJSF calculation using the "Open in Excel" option from an ADO query
result.

## Starfish Retrospective (Quarterly)

This is a broader health check where team members privately fill out a series of notes using
categories: Start Doing, Stop Doing, Keep Doing, Do More, Do Less. The inputs are collected
anonymously and then in the meeting, the notes are clustered into themes. The team discusses
high‑count clusters first and extracts change actions. For more information, search the internet for
"[starfish retrospective](https://www.bing.com/search?q=starfish+retrospective)".

## Meeting Anti‑Patterns

- Status recital especially if it covers info already visible on board.
- Design debates in standup instead of small focused follow‑ups.
- Silent standup. A lack of questions means missed collaboration.
- Carrying unresolved retro actions from session to session.
- Planning inflation wars where team members are arguing numbers instead of clarifying assumptions.
- Team members skipping these meetings. If the meetings aren't a valuable use of time, discuss it in
  the retrospective meeting.

## Related Links

[← Step 6: Design Docs](design-docs.md) | [Step 8: WIP & Flow →](wip-and-flow.md)

- Communication - [Communication Patterns](communication.md)
