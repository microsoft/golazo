# Why Golazo Works

## Summary

Golazo exists because many teams encounter the same recurring problems even when the engineers are
capable and the intent is good. Work starts before the approach is clear. Reviews become design
meetings. Urgent work arrives on top of already full queues. Knowledge concentrates in a few people.
The result is not just slower delivery. It is also more stress, more rework, and less confidence in
the system.

Golazo attempts to address those issues through a small set of mutually reinforcing practices. The
method does not promise perfect flow. It tries to create conditions where problems become visible
earlier and therefore cheaper to correct.

## Problem, Mechanism, and Outcome

| Problem Symptom                            | Golazo Mechanism                             | Expected Outcome                                 |
| ------------------------------------------ | -------------------------------------------- | ------------------------------------------------ |
| PR churn over design questions             | Short design doc before implementation       | Reviews focus more on details and less on rework |
| Persistent bug or incident backlog         | Explicit triage and a dedicated Swarm rail   | Faster response and more pressure to fix causes  |
| Planning that cannot absorb new priorities | Frequent reordering and small ticket slices  | Backlog changes become less disruptive           |
| Overloaded on-call rotation                | Shared operational ownership and automation  | Less dependence on one person for urgent issues  |
| Slow reviews                               | Smaller changes and visible review state     | More predictable review latency                  |
| Knowledge silos                            | Shared docs and open ticket selection        | Broader context across the team                  |
| Slow onboarding                            | Small tickets and reusable design history    | New engineers become productive sooner           |
| Single points of failure                   | Workstream rotation and shared review        | Reduced dependency on individual experts         |
| Multitasking overload                      | Individual and column WIP limits             | Better focus and lower context switching         |
| Large failed efforts                       | Ticket sizing and early validation           | Lower sunk cost when ideas do not work out       |
| Low engagement                             | Autonomy to pull from Ready                  | Greater agency without losing shared priorities  |
| Weak ownership                             | Shared signoff and team-level accountability | Problems are treated as system issues, not blame |

These are intended outcomes, not guarantees. A team can adopt the mechanics and still get poor
results if it ignores the behavioral parts, especially shared ownership and honest retrospectives.

## Key Challenges Explained

### Pull Request Churn

When implementation starts before the problem and approach are aligned, the pull request becomes the
place where basic decisions are revisited. That is expensive. Reviewers see the code late. Authors
have already invested heavily in a direction. Golazo moves more of that discussion into the Analyze
step so the cost of changing direction is lower.

### Incident and Bug Backlog

A growing defect queue usually means the team is paying for earlier quality gaps. The issue is not
just prioritization. It is often a signal that design clarity, testing, observability, or release
discipline is weaker than expected. Golazo tries to make that visible by forcing urgent issues into
the board rather than letting them live in scattered side channels.

### Planning Rigidity

Long planning horizons are often treated as a coordination aid, but they can become a trap when the
environment changes faster than the plan. Golazo assumes reprioritization is normal. That only works
if work items are small enough that changing direction does not mean abandoning months of partially
finished work.

### On Call Engineer Overload

Many teams informally treat the on-call engineer as a buffer for unresolved operational debt. That
scales poorly. Golazo keeps the role, but tries to narrow it to triage and coordination by pushing
quality work upstream and by normalizing team involvement when something truly urgent appears.

### Review Latency

Review queues often grow for understandable reasons. Large changes are hard to context-switch into,
and reviewers are unsure whether they are expected to evaluate code quality, product intent, or
architecture. Smaller tickets and design docs do not eliminate the queue, but they reduce the
activation energy required to review usefully.

### Knowledge Silos and Ramp

If only one or two people regularly work in a given area, the team is always one interruption away
from delay. Golazo addresses that in several ways at once: open ticket selection, lightweight design
docs, pairing, and shared reviews. None of these is sufficient on its own. Together they make
context more portable.

### Focus and Multitasking Stress

High utilization can look productive while actually slowing delivery. Too much parallel work creates
waiting, context loss, and a steady stream of partially finished tasks. WIP limits are a blunt tool,
but they are effective because they force teams to confront those tradeoffs directly.

### Large Initiative Risk

Large efforts usually fail gradually before they fail visibly. Requirements drift, unknowns expand,
and dependencies accumulate. Golazo attempts to reduce that risk by insisting on value-sliced work
with explicit validation points. This does not remove strategic risk, but it reduces the amount of
time spent discovering that a direction is weak.

### Motivation and Ownership

Teams are more resilient when engineers can influence what they pick up and when success is not
framed as individual heroics. Shared ownership has real costs, including the need for better written
context and more deliberate review habits, but those costs are usually lower than the cost of strong
single-owner dependency.

## How Do We Know It’s Working?

There is no single definitive metric.

The board should show healthier flow over time. Reviews should become smaller and less contentious.
The team should see fewer surprise incidents and less hidden work. Onboarding should become easier
because prior decisions are easier to reconstruct. Morale should improve if the process is reducing
friction rather than just changing its shape.

Some of those outcomes are measurable, some are only directionally observable, and some depend on
local context. More work is usually needed to separate genuine process improvement from other
changes, such as staffing or product volatility.

## Influences

Golazo borrows from Lean, Kanban, and Agile traditions, especially around flow, visibility,
incremental delivery, and feedback. It also places more emphasis than many lightweight processes do
on short written design artifacts as a practical coordination tool.

The process is intentionally minimal, but it is not minimal in the sense of "do almost nothing." It
is minimal in the sense of trying to keep only the practices that materially improve flow and
learning.

## Navigation

[Step 2: Principles →](principles.md)
