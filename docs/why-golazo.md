# Why Golazo Works

## Summary

Work starts before the approach is clear. Reviews become design meetings. An urgent bug lands when
everyone already has something in progress. Golazo helps teams catch problems like these while
there's still time to do something about them.

## Problem, Mechanism, and Outcome

| Problem Symptom                            | Golazo Mechanism                             | Expected Outcome                                 |
| ------------------------------------------ | -------------------------------------------- | ------------------------------------------------ |
| PR churn over design questions             | Short design doc before implementation       | Reviews focus more on details and less on rework |
| Persistent bug or incident backlog         | Triage and a dedicated Swarm rail            | Respond sooner and see which problems recur      |
| Planning that cannot absorb new priorities | Frequent reordering and small ticket slices  | Backlog changes become less disruptive           |
| Overloaded on-call rotation                | Shared operational ownership and automation  | Less dependence on one person for urgent issues  |
| Slow reviews                               | Smaller changes and visible review state     | More predictable review times                    |
| Knowledge silos                            | Shared docs and open ticket selection        | Broader context across the team                  |
| Slow onboarding                            | Small tickets and reusable design history    | New engineers become productive sooner           |
| Single points of failure                   | Workstream rotation and shared review        | Reduced dependency on individual experts         |
| Multitasking overload                      | Individual and column WIP limits             | Fewer tasks to switch between                    |
| Large failed efforts                       | Ticket sizing and early validation           | Lower sunk cost when ideas do not work out       |
| Low engagement                             | Let engineers pull from Ready                | Engineers choose from work the team prioritized  |
| Weak ownership                             | Shared signoff and team-level accountability | The team investigates what went wrong together   |

Use these outcomes as things to look for. A new board won't help much if nobody picks up a review or
the same blockers go unmentioned in every retrospective.

## Key Challenges Explained

### Pull Request Churn

If a reviewer disagrees with the approach after the code is written, the author may have to start
over. Discuss the approach in Analyze, while changing it still means editing a short doc.

### Incident and Bug Backlog

If the same bugs keep coming back, look for gaps in design, testing, monitoring, or release
practices. Put urgent issues on the board so the whole team can see what keeps interrupting planned
work.

### Planning Rigidity

Plans change. Small tickets let the team reorder what comes next without abandoning months of
partially finished work.

### On Call Engineer Overload

The on-call engineer triages and coordinates. When an incident needs more hands, the team helps.
Testing and monitoring during normal delivery can also keep recurring problems from landing on the
next person on call.

### Review Latency

A large pull request takes time to understand, especially when reviewers have to work out why the
change is needed. A smaller change and a link to the design doc make it easier to get started.

### Knowledge Silos and Ramp

If only one person knows an area, work can stall when they're away. Let engineers pull tickets
outside their usual areas, pair when they need help, and leave design notes the next person can
read.

### Focus and Multitasking Stress

Everyone can be busy while little gets finished. When a column hits its work-in-progress limit, help
move a ticket forward before pulling another.

### Large Initiative Risk

The longer you wait to test a direction, the more work you may have to undo. Split large efforts
into pieces a stakeholder can try and validate before the team commits to the next one.

### Motivation and Ownership

Engineers can choose what to pick up from Ready. That only works if people write down decisions and
make time for each other's reviews. Otherwise, unfamiliar work still ends up with the same person.

## How Do We Know It’s Working?

Look for smaller reviews, fewer surprise incidents, and less work happening off the board. Ask new
teammates whether they can find past decisions, and ask the team whether the work feels more
manageable.

Look at those signals together. If staffing or product priorities changed at the same time, a better
metric by itself doesn't tell you what helped.

## Influences

Golazo borrows from Lean, Kanban, and Agile: show work as it happens, deliver it in small pieces,
and get feedback early. Short design docs help the team coordinate without adding a meeting for
every decision.

## Navigation

[Step 2: Principles →](principles.md)
