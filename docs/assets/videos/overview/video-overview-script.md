# Golazo Overview – Full Narration Script (≈10 Minutes)

## Hook & Pain Framing

(Opening, direct eye contact) If your team ideates fast but ships slow, if reviews feel like
surprise architecture debates, if work vanishes into silos, and 'done' secretly means 'merged but
not validated' then you're in the right place. Golazo is built to remove those friction points and
more. We’ve all lived the slow review queue, the chat interruptions, the multitasking drag, and the
fragile single-owner pattern. Golazo focuses on flow, quality from the start, and shared
understanding early.

In the next few minutes I’ll show you the few lightweight habits that change the feel of delivery
without adding process bloat.

Golazo gives you less friction, faster flow, happier customers, and happier teams.

## What Is Golazo

Golazo is a lightweight engineering methodology for small to mid-sized teams—think four to ten
engineers—designed to keep batch sizes small, make status instantly visible, and define 'done' by
observed value.

Four key artifacts support the process:

1. Small, value-focused tickets.
2. Targeted, collaborative design docs with two signoffs.
3. A visual task board with priority rails and ticket stage columns.
4. Regular lightweight team touchpoints (like standups, retros, and joint planning) to tune flow,
   eliminate waste, and adapt priorities together.

Think of the lifecycle as: clarify together early → build small → streamline reviews → share
learnings.

## Mapping Pains to Practices

Each practice is there for a reason, not for ceremony.

- Do you see a lot of rework happening late in reviews? We shift architectural alignment earlier
  with design docs.
- Are feedback loops too slow? We slice value small and visualize flow so blockers surface quickly.
- Are there knowledge silos on the team? With Golazo, anyone can pick up any Ready ticket. Pairing
  is encouraged. Reviews and design docs help spread and create fluid context.
- Do team members suffer from multitasking overload? WIP limits cap active work so attention isn’t
  spread too thin.
- Does finished work circle around to come back as bug reports or rough on call shifts? The
  validation stage demands that value be observed and confirmed before the ticket is closed.
- Are your standup meetings status reports? Golazo standups focus on what has been learned and what
  the team can do to help move the ticket to the next stage.

So Golazo is targeted at reducing friction — it's not a new layer of meetings.

## Design Docs (Core Mechanism)

Design docs are deliberately focused. They’re scaffolding for alignment, not novels.

The sections convey Context, Goal, Constraints, Design, and Task List. That’s enough to catch
mismatched assumptions early. Two signoffs ensure ideas aren’t isolated and invite fast asynchronous
clarification, so by the time you start coding you’re not guessing. And when the ticket is done,
that doc persists which creates a searchable context library to reduce single‑expert risk and power
AI tools.

The result is that code reviews focus on implementation quality, not big-picture debates at the last
minute.

## Task Board & Priority Rails

The task board is our shared instrumentation panel. It's a window into team flow, focus, and
emerging bottlenecks.

Columns trace the journey: Backlog ideas, Ready, Design, Engineering, Release, Validation, Done.
Rails help dedicate funding and visually separate urgency: Swarm, Interrupt, Planned. Swarm is for
urgent collaborative focus, Interrupt to allow changes in flight without consuming all the team's
resources, Planned for normal flow. A quick glance tells you: Are we waiting for reviews? Is the
Interrupt rail growing? Is a specific work item struggling? Are we running too fast and creating too
many swarms? And because team members can see a variety of projects for them to select from the
Ready column, knowledge spreads naturally. You’re not waiting for assignment which increases
autonomy and shrinks knowledge bottlenecks.

## WIP Limits & Flow

Work In Progress limits are the discipline that focuses effort where it adds the most team value.

High WIP looks busy but finishes slowly. Low WIP looks calmer but finishes consistently with higher
quality. By capping active items per engineer or team, we force unblock behavior: finish or free
someone before pulling new work. This enables rapid swarm response when an incident hits—because
people aren’t juggling five half-started tasks. Starting less equals finishing more!

## Small Tickets & Slicing

Small tickets are the fuel of flow.

Our guidelines when creating a ticket are clear user value, less than two weeks to implement,
explicit validation plan, and nothing blocking the work. Instead of a giant feature implemented
bottom-up, we slice by value. Each slice delivers something observable. This compresses feedback
cycles and lowers integration risk. You make small course corrections early instead of bolting
changes onto a large unstable branch.

## Integrated Review & Knowledge Spread

Because alignment happened earlier, code reviews narrow in scope.

Now reviewers concentrate on correctness, clarity, and edge cases—not whether the approach should
exist at all. Design docs provide enough context for anyone to participate in a code review and add
their own unique value while also learning more about other areas of the code.

## Customer Validation Stage

Golazo treats observed value as the finish line, not just when code is merged into the main branch.

Validation examples include: stakeholder signoff, the is feature actually used, metric improvement
verified, internal dogfooding success, or pilot user feedback. If validation fails, the ticket moves
backward so there is no hidden post-merge churn. The board tells the truth. This reframes success:
we shipped impact, not just artifacts.

## Team Morale

Golazo lifts morale by pairing autonomy with safety and support. Engineers are empowered to pick up
any ticket from any workstream in the Ready column and they can gain or share context through design
documents and discussions. Tiny pairs and micro‑swarms emerge: a 15‑minute exploration of an edge
case, an early shared look at a design choice, or a second set of eyes before code hardens. Each
prevents late churn and transfers context. Public channels of discussion and review checkpoints turn
quiet observers into helpers. If you see that the chat is silent it’s a prompt to lean in, not proof
that everything is green. And if a ticket does slip, the conversation is systemic, not personal.

## Closing & Call to Action

All this comes together in a mindset shift: we succeed and fail together. A missed edge case isn’t
one engineer’s lapse—it’s shared learning because many eyes were invited early. Every clarified
assumption, simpler design suggestion, or surfaced risk accelerates our delivery. Reviews become a
brief moment of collective ownership, eroding hero bottlenecks and expanding safe entry into any
part of the codebase. We are walking forward together as a team.

That's Golazo: Scoped work items with defined value, early alignment, distributed knowledge, and
shared success. It's simple, but it works. Start your reading with the 'Why Golazo' doc for more
context and keep reading for deeper details.
