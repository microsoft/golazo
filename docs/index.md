# Golazo

## Summary

Golazo is a lightweight engineering methodology for small and mid-sized teams. It is designed to
reduce the kinds of delivery friction that are common in real environments: code reviews that reopen
basic design questions, too much parallel work, unclear ownership, slow feedback loops, and teams
that rely too heavily on private context.

Golazo asks teams to keep work small, agree on the approach before implementation, limit work in
progress, and treat customer validation as part of completion rather than as a separate concern. The
goal is to produce a system that is easier to reason about and easier to improve.

<figure>
<video controls preload="metadata" width="720">
  <source src="assets/video-overview.mp4" type="video/mp4" />
  Your browser does not support embedded videos. You can download it instead: <a href="assets/video-overview.mp4">Golazo Overview (MP4)</a>.
</video>
<figcaption>Golazo overview: a short introduction to the method and its core practices.</figcaption>
</figure>

## Who It’s For

- Teams that want more predictable flow and less hidden work
- Teams working in person, hybrid, or across time zones
- Product or platform groups that are small enough to benefit from shared context
- Teams that need a practical way to reduce review churn and operational drag
- Organizations trying to improve delivery reliability without adding heavy process overhead

In practice, the model tends to fit teams of roughly 4 to 10 engineers best, though parts of it can
be adapted outside that range.

## What Makes It Different

- Design alignment happens before implementation through a short design document and peer signoff
- Work in progress is constrained deliberately rather than informally
- The task board is treated as the shared model of reality, not as an after-the-fact reporting tool
- Tickets are kept small enough that planning can adapt without large sunk-cost debates
- Review is part of flow, not a separate bottleneck management problem
- Shared ownership is built into the process by allowing engineers to pull from a common Ready queue
- Customer validation is explicit, which makes "done" stricter than "merged"

This is technically simple. The harder part is behavioral consistency.

## Inspiration

Golazo builds on ideas found in several books:

- "Implementing Lean Software Development: From Concept to Cash" by Mary and Tom Poppendieck
- "The Principles of Product Development Flow: Second Generation Lean Product Development" by Donald
  G. Reinertsen
- "Kanban: Successful Evolutionary Change for Your Technology Business" by David J. Anderson
- "The Lean Startup: How Today's Entrepreneurs Use Continuous Innovation to Create Radically
  Successful Businesses" by Eric Ries

The documents in this repository describe one practical synthesis of those ideas. They are not meant
to imply that the underlying sources agree on every detail or that Golazo is a formal standard.

## Suggested Reading Path

The navigation links at the bottom of each page follow a suggested reading order. You can also use
the left navigation in the rendered site.

1. [Why Golazo](why-golazo.md)
2. [Principles](principles.md)
3. [Task Board](task-board.md)
4. [Roles & Responsibilities](roles.md)
5. [Tickets](tickets.md)
6. [Design Docs](design-docs.md)
7. [Meetings](meetings.md)
8. [WIP & Flow](wip-and-flow.md)
9. [Communication](communication.md)
10. [Adoption Guide](adoption-guide.md)
11. [FAQ](faq.md)
