# WIP, Flow & Limits

> Public draft – adapted from legacy WIP section with additional flow theory context.

## Summary

Limiting Work In Progress (WIP) increases throughput, improves predictability, and reduces stress by
finishing the most valuable work sooner instead of diluting focus across many partially‑done items.

## Why Limit WIP

- **Faster Completion** – Partially done work delivers zero value; finishing earlier accelerates
  feedback loops.
- **Lower Context Switching Cost** – Humans pay a heavy cognitive tax when juggling many threads;
  fewer active tickets = higher sustained quality.
- **Expose Bottlenecks** – When a column hits its limit you must _improve flow_ (help upstream)
  instead of silently starting more work.
- **Enable Swarming** – Reserved capacity makes it cheap to swarm critical incidents without
  derailing weeks of in‑flight work.
- **Reduce Stress** – Predictable small queues beat long hidden backlogs of half‑finished tasks.

## Policies (Baseline Recommendations)

- **Individual Limit** – A person’s name should appear as active Shepherd on at most 2 tickets
  (often 1 for new team members).
- **Column Limits** – All intermediate columns (Ready optional) have numeric limits sized to team
  capacity. If the next column is full you _stop starting_ and help finish.
- **Interrupt Rail Limit** – Only one active Interrupt at a time. Others wait in Ready; protects the
  Planned rail.
- **Swarm Handling** – Swarm items temporarily override individual limits. Once stabilized, excess
  helpers peel off.
- **Ticket Size** – Tickets must be small enough to fit under the SLA (commonly < 2 weeks) so WIP
  represents near‑term deliverables, not projects.

## Managing Flow in Practice

When a limit blocks movement:

1. Highlight blockage in standup (or async channel if discovered mid‑day).
2. Redirect available capacity to tickets closest to Done (right‑most first).
3. If chronic, adjust process—not just the number (e.g., reduce Analyze batching, add template
   guidance).

## Detecting Bottlenecks

Look for: columns consistently at or over limit; aging tickets (high cycle time) compared to
neighbors; repeated backward movement; spike in blocked markers. See
[Measuring Success](measuring-success.md) for quantitative signals (e.g., WIP Age, Cycle Time
trends).

## Flow Theory (Lightweight)

Little’s Law (informally):

```
Average Throughput ≈ WIP / Average Cycle Time
```

For a fixed WIP, reducing cycle time increases throughput. For a fixed cycle time, excess WIP only
increases delay. Therefore we cap WIP intentionally and focus on finishing work rather than starting
more.

## Anti‑Patterns

- Increasing limits instead of solving root causes.
- Large tickets that “camp” in Engineer for weeks.
- Hidden parallel work (side branches) not visualized on the board.
- Interrupt rail frequently >1 or treated as a parking lot.

## Related

- Workflow Overview → [Workflow Overview](workflow-overview.md)
- Tickets → [Tickets & Sizing](tickets.md)
- Measuring Success → [Measuring Success](measuring-success.md)
