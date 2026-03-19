# Roles and Responsibilities

## Summary

Golazo uses a small number of explicit roles. The intent is not to create hierarchy inside the team.
It is to make a few recurring responsibilities visible so that important process work does not
happen accidentally or get concentrated in one person by default.

## Core Roles

### Coach

The coach is responsible for the health of the workflow rather than for directing the content of the
work. In practice, this means watching for drift, bottlenecks, and weak process discipline.

**Key Responsibilities**

- Facilitate standup and retrospectives
- Enforce WIP limits and call out bottlenecks explicitly
- Protect the design doc and review expectations from erosion
- Maintain planning cadence and backlog hygiene
- Push for root-cause analysis when tickets move backward or age unexpectedly
- Help other team members learn the coaching role over time

The coach should influence how the team works, not become the person who decides who does what.

**Anti-Patterns**: assigning work to individuals by habit, owning every process decision, silently
relaxing standards when pressure rises

### On Call Engineer

The on-call engineer is a rotating role that handles the first response to incidents and other
unexpected work. The role exists to coordinate urgent intake, not to absorb all urgent execution.

**Key Responsibilities**

- Triage new incidents and interrupts and ensure they are represented on the board
- Create or update Swarm tickets before standup when urgent work already exists
- Perform lightweight initial investigation where fast resolution is possible
- Communicate status clearly and hand off cleanly at rotation boundaries
- Identify repetitive operational work and propose automation or documentation improvements

**Time Expectation**: on mature teams, on-call work is often measured in minutes per day rather than
hours. If it consistently consumes much more time, that usually points to upstream quality,
observability, or ownership issues.

**Anti-Patterns**: hoarding urgent fixes, becoming the default operations silo, letting important
context stay in chat instead of on the board or in documentation

## Navigation

[← Step 3: Workflow Overview](task-board.md) | [Step 5: Tickets →](tickets.md)
