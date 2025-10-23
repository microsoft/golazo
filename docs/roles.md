# Roles & Responsibilities

> Public draft – adapted from legacy Roles section + relevant FAQ guidance.

## Summary

Golazo keeps formal roles to a minimum. A small set of clearly defined responsibilities sustains
flow, reinforces shared ownership, and creates space for equitable growth.

## Core Roles

### Coach

The process facilitator and quality bar champion. The Coach observes _how_ work flows and nudges the
team when drift appears.

**Key Responsibilities**

- Facilitate standup (ticket‑first order) and retrospectives.
- Enforce WIP limits & highlight bottlenecks rather than silently adjusting.
- Guard the integrity of design doc + review practices.
- Ensure planning cadence and backlog hygiene.
- Prompt root‑cause exploration for backward ticket movement.
- Mentor emerging coaches to distribute facilitation skill.

**Anti‑Patterns**: Owning all decisions; rewriting tickets; acting as a project manager assigning
work.

### DRI (Designated Responsible Individual)

Rotating role (often weekly) monitoring inbound signals (incidents, urgent asks) and initiating the
proper response without becoming a bottleneck.

**Key Responsibilities**

- Triage new incidents / interrupts; create or update tickets.
- Ensure Swarm tickets exist _before_ standup with context.
- Perform lightweight first‑pass investigation (many items resolved in minutes).
- Communicate status & handoff cleanly to next DRI.
- Capture repetitive tasks → propose automation or documentation improvements.

**Time Expectation**: Mature teams often spend < 30–60 mins/day on DRI tasks; excess time signals
upstream quality or monitoring issues.

**Anti‑Patterns**: Hoarding all urgent fixes, becoming the de facto operations silo, deferring
documentation.

## Ownership Model

Golazo optimizes for _team_ ownership. Any engineer can pick any Ready ticket. The **Shepherd**
listed is the facilitator ensuring:

- Design doc prepared & signed off.
- Reviews happen promptly.
- Definition of Done fully met (tests, monitoring, docs).
- Customer validation step closes the loop.

Shepherd ≠ solo implementer; pairing and micro‑swarming encouraged. Knowledge rotates naturally as
interests vary and coaches watch for area monopolies.

## Growth & Equity

Design encourages equitable access to impactful work:

- Rotating DRI + open ticket selection prevents gatekeeping.
- Junior engineers gain confidence through design doc signoffs—shared responsibility, not isolation.
- Senior engineers demonstrate leadership by refining backlog items, mentoring during Analyze,
  enforcing quality fundamentals, and shaping architectural consistency.
- Career progression discussions map leadership expectations (technical depth, cross‑team influence)
  to Golazo artifacts (design docs authored, cross‑area pairing, backlog curation).

## Optional Roles (Lightweight Stewardships)

- **Metrics Steward** – Maintains dashboard queries / scripts; surfaces trends for retros.
- **Documentation Steward** – Curates glossary & templates; ensures new patterns recorded.
- **Quality Champion** (rotating) – Focuses sprint/period on test debt & observability gaps. These
  roles should not create silos—authority remains distributed.

## Related

- Meetings → `meetings-and-ceremonies.md`
- Tickets → `tickets.md`
- Communication → `communication.md`
