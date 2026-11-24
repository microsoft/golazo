# Work in Progress Limits

## Summary

Limit work in progress (WIP) so the team can finish more of what it starts. When a column is full,
look for a ticket you can help move before pulling another.

## Why Limit WIP

- Get feedback sooner by finishing a ticket instead of starting another.
- Spend less time switching between tasks and remembering where you left off.
- See where tickets are piling up when a column reaches its limit.
- Leave people free to help when an incident needs a Swarm.
- Make the workload easier to see and manage.

## Policies

- Individual Limit: one person should usually shepherd no more than 2 active tickets.
- Column Limits: set explicit limits for intermediate columns based on what the team can handle. If
  the next column is full, help finish a ticket there before starting another.
- Interrupt Rail Limit: only one active Interrupt should exist at a time unless the team has a very
  specific reason to break that rule.
- Swarm Handling: Swarm work can temporarily override normal limits, but people should peel off once
  the urgent situation is stable.
- Ticket Size: tickets need to remain small enough that WIP reflects near-term work rather than
  disguised projects.

Adjust the numbers to suit your team, and use the agreed limits when deciding what to start.

## Managing Flow in Practice

Watch for a few common signals:

- columns that are regularly at or above their limit
- tickets that have been open much longer than others in the same column
- repeated backward movement
- recurring blocked markers or dependency waiting

When a limit blocks movement:

1. Call it out in standup.
2. Ask anyone with time to help with the ticket closest to Done.
3. If the same column keeps filling up, find out why before raising the limit.

## Flow Theory (Lightweight)

[Little’s Law](https://www.bing.com/search?q=little%27s+law) relates three averages for a stable
workflow:

```
Average Throughput = Average WIP / Average Cycle Time
```

If throughput stays the same, more work in progress means a longer average cycle time. If average
WIP stays the same, a shorter average cycle time corresponds to higher throughput.

## Anti‑Patterns

- Raising WIP limits instead of fixing the reason work is getting stuck
- Allowing large tickets to remain in Engineer for long periods
- Doing parallel work that never appears on the board
- Normalizing multiple active Interrupts as routine behavior

## Navigation

[← Step 7: Meetings](meetings.md) | [Step 9: Communication →](communication.md)
