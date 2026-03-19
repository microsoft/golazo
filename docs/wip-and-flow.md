# Work in Progress Limits

## Summary

Work in progress limits are one of the central control mechanisms in Golazo. They exist because too
much parallel work slows the system even when individual engineers appear busy. The immediate goal
is not discipline for its own sake. It is to increase the rate at which valuable work is actually
finished.

## Why Limit WIP

- Faster Completion: partially finished work does not deliver value, and finishing earlier shortens
  the feedback loop.
- Lower Context Switching Cost: fewer active threads generally means fewer mistakes and less mental
  overhead.
- Expose Bottlenecks: when a column reaches its limit, the team is forced to notice the constraint.
- Enable Swarming: keeping some capacity free makes urgent shared work possible.
- Reduce Stress: small, visible queues are easier to reason about than a large collection of hidden
  half-finished tasks.

This is one of the places where the theory and the lived experience usually match fairly well.

## Policies

- Individual Limit: one person should usually shepherd no more than 2 active tickets.
- Column Limits: intermediate columns should have explicit limits sized to team capacity. If the
  next column is full, the team helps work ahead move instead of starting more.
- Interrupt Rail Limit: only one active Interrupt should exist at a time unless the team has a very
  specific reason to break that rule.
- Swarm Handling: Swarm work can temporarily override normal limits, but people should peel off once
  the urgent situation is stable.
- Ticket Size: tickets need to remain small enough that WIP reflects near-term work rather than
  disguised projects.

The exact numbers should be adapted to the team, but the discipline should remain real.

## Managing Flow in Practice

Watch for a few common signals:

- columns that are regularly at or above their limit
- tickets aging much longer than nearby peers
- repeated backward movement
- recurring blocked markers or dependency waiting

When a limit blocks movement:

1. Call it out in standup.
2. Send available capacity toward work closest to completion.
3. If the pattern persists, inspect the underlying cause instead of only raising the number.

## Flow Theory (Lightweight)

[Little’s Law](https://www.bing.com/search?q=little%27s+law) gives a useful mental model:

```
Average Throughput ≈ WIP / Average Cycle Time
```

In plain terms, if cycle time is fixed, adding more WIP mainly increases delay. If WIP is kept
stable and cycle time falls, throughput improves. Real systems are messier than the formula, but the
direction of the tradeoff is still useful.

## Anti‑Patterns

- Raising WIP limits instead of fixing the reason work is getting stuck
- Allowing large tickets to remain in Engineer for long periods
- Doing parallel work that never appears on the board
- Normalizing multiple active Interrupts as routine behavior

## Navigation

[← Step 7: Meetings](meetings.md) | [Step 9: Communication →](communication.md)
