# Work in Progress Limits

## Summary

Limiting Work In Progress (WIP) increases throughput, improves predictability, and reduces stress by
finishing the most valuable work sooner instead of diluting focus across many partially‑done items.

## Why Limit WIP

- Faster Completion: Partially done work delivers zero value and finishing earlier accelerates
  feedback loops.
- Lower Context Switching Cost: Humans pay a heavy cognitive tax when juggling many threads, and
  fewer active tickets equals higher sustained quality.
- Expose Bottlenecks: When a column hits its limit you must _improve flow_ (help upstream) instead
  of silently starting more work.
- Enable Swarming: Reserved capacity makes it cheap to swarm critical incidents without derailing
  weeks of in‑flight work.
- Reduce Stress: Predictable small queues beat long hidden backlogs of half‑finished tasks.

## Policies

- Individual Limit: A person’s name should appear as active Shepherd on at most 2 tickets.
- Column Limits: All intermediate columns have numeric limits sized to team capacity. If the next
  column is full you _stop_ and help a ticket ahead of you finish. The execution columns should sum
  to 1.5 \* Team Size as a starting point.
- Interrupt Rail Limit: Only one active Interrupt at a time. Others wait in Ready which protects the
  Planned rail from interruptions.
- Swarm Handling: Swarm items temporarily override individual limits. Once stabilized, excess
  helpers peel off.
- Ticket Size: Tickets must be small enough to fit under the SLA (commonly < 2 weeks) so WIP
  represents near‑term deliverables, not projects. Small tickets mean that someone is frequently
  becoming idle and free to work on Swarms, etc.

## Managing Flow in Practice

Look for columns consistently at or over limit, aging tickets compared to neighbors, repeated
backward movement, and spikes in blocked markers.

When a limit blocks movement:

1. Highlight the blockage in standup.
2. Redirect available capacity to tickets closest to Done.
3. If this is a chronic condition, adjust the process and culture not just the WIP number.

## Flow Theory (Lightweight)

[Little’s Law](https://www.bing.com/search?q=little%27s+law):

```
Average Throughput ≈ WIP / Average Cycle Time
```

For a fixed WIP, reducing cycle time increases throughput. For a fixed cycle time, excess WIP only
increases delay. Therefore we cap WIP intentionally and focus on finishing work rather than starting
more.

## Anti‑Patterns

- Increasing WIP limits instead of solving root causes.
- Large tickets that “camp” in Engineer for weeks.
- Hidden parallel work and side branches not visualized on the board.
- Interrupt rail frequently with more than one active ticket.

## Navigation

[← Step 7: Meetings](meetings.md) | [Step 9: Communication →](communication.md)
