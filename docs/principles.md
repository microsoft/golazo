# Principles

## Summary

The principles below are the operating assumptions behind Golazo. They matter because the process
mechanics only make sense if the team agrees on what those mechanics are trying to optimize.

The common thread is straightforward: finish valuable work in small increments, keep quality work
upstream, and avoid building a system that depends on constant firefighting or concentrated personal
context.

## Core Principles

### Deliver Quickly

Deliver small slices of value instead of holding work for large releases or broad reveals. The main
benefit is not speed for its own sake. It is that smaller delivery intervals create faster learning
and lower the cost of being wrong.

### Eliminate Waste

Treat waste as anything that consumes attention without improving customer value or future team
effectiveness. Examples include excess WIP, avoidable waiting, repetitive manual steps, and debates
that continue because the underlying assumptions were never written down.

### Defer Commitment

Do not lock in details earlier than necessary. Early certainty is often artificial. At the same
time, deferring commitment is not the same as avoiding preparation. The intent is to preserve
options until the team has enough information to choose well.

### Build Quality In

Quality work has to happen during normal delivery, not after it. Testing, observability, review, and
design clarity are part of the job of finishing the ticket. If they are treated as optional or
downstream cleanup, the team eventually pays for that choice through defects and operational load.

### Create Knowledge

A healthy team creates reusable knowledge as it works. Short design docs, review comments, and
deliberate ticket rotation all contribute to that. The goal is not documentation for its own sake.
It is to make the system easier to understand when the original author is unavailable or the context
has faded.

### Respect People

Protect focused time and avoid loading people beyond what they can reasonably complete. Systems that
depend on constant multitasking and emergency behavior usually appear productive in the short term,
but they are harder to sustain and harder to improve.

### Succeed and Fail Together

Golazo assumes the team is the unit of performance. Wins and failures both provide information about
the system. Shared ownership does not remove accountability, but it does change where the first
question goes. Instead of asking which person failed, the team asks what conditions made the failure
likely.

### Optimize the Whole

Local efficiency is not the same as overall throughput. An engineer starting a new task may look
busy, but helping an almost-finished task move forward is often more valuable. The process tries to
optimize for completed, validated work rather than visible individual activity.

## Applying the Principles

- Deliver Quickly: keep tickets under the team SLA and prefer slices that a stakeholder can validate
  independently.
- Eliminate Waste: visualize blockers, note backward movement, and inspect recurring sources of
  delay in retrospectives.
- Defer Commitment: capture ideas in the backlog without forcing detailed design before the work is
  close to being started.
- Build Quality In: define tests, monitoring, and documentation expectations before implementation
  begins.
- Create Knowledge: use design docs and review expectations to spread context instead of preserving
  it in private conversations.
- Respect People: keep WIP limits real enough to reduce cognitive load and make help available when
  priorities change.
- Succeed and Fail Together: treat incidents, missed estimates, and rework as opportunities to
  improve the system rather than assign personal blame.
- Optimize the Whole: direct idle capacity toward finishing, reviewing, and unblocking before new
  work is pulled.

## Navigation

[← Step 1: Why Golazo](why-golazo.md) | [Step 3: Workflow Overview →](task-board.md)
