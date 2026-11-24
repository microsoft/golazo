# Roles and Responsibilities

## Summary

The coach helps the team spot delays and improve how it works. The on-call engineer is the first
point of contact for incidents and other urgent work.

## Core Roles

### Coach

The coach watches where work gets stuck and helps the team fix recurring problems. Engineers still
choose their own tickets from Ready.

**Key Responsibilities**

- Facilitate standup and retrospectives
- Enforce WIP limits and call out bottlenecks explicitly
- Make sure design docs and reviews still happen when work gets busy
- Keep planning on schedule and the top of the backlog up to date
- Ask what went wrong when tickets move backward or take longer than expected
- Help other team members learn the coaching role over time

**Anti-Patterns**: assigning work to individuals by habit, owning every process decision, silently
relaxing standards when pressure rises

### On Call Engineer

Engineers take turns on call. The person on call assesses the issue and brings in the team when they
need help.

**Key Responsibilities**

- Triage new incidents and interrupts and ensure they are represented on the board
- Create or update Swarm tickets before standup when urgent work already exists
- Check whether there's a quick fix
- Share the current status and hand off open issues to the next person on call
- Identify repetitive operational work and propose automation or documentation improvements

**Time Expectation**: on mature teams, on-call work is often measured in minutes per day rather than
hours. If it regularly takes much longer, look for recurring defects, gaps in monitoring, or unclear
ownership.

**Anti-Patterns**: trying to fix every urgent issue alone, becoming the only person who knows how to
handle incidents, leaving important details in chat instead of recording them on the board or in a
doc

## Navigation

[← Step 3: Workflow Overview](task-board.md) | [Step 5: Tickets →](tickets.md)
