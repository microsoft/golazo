# Frequently Asked Questions

> Public draft – answers scoped to topics not already covered in depth elsewhere. For foundational
> context see: `why-golazo.md`, `adoption-guide.md`, `design-docs.md`,
> `planning-and-prioritization.md`.

## Using This FAQ

Scan section headings first; each answer links to deeper material. If a question seems missing, it
may now have its own dedicated page.

## Team Operation

**How big should a team be?** 6–8 engineers is a sweet spot: enough diversity for collaboration,
small enough for shared context. Larger groups can split boards and sync leads periodically.

**Can a single engineer use Golazo practices?** Yes—visualize work, draft mini design docs, enforce
personal WIP, and request external peer reviews for key changes.

**What if a ticket stalls?** Raise in standup immediately. If aging continues, Value Stream Map it
to identify hidden dependencies, over‑sizing, or unclear definition of done.

## Adoption & Transition

**How long is the trial?** A focused 90‑day period (see `adoption-guide.md`). Shorter trials rarely
expose the compounding benefits.

**Do we customize early?** Not unless there is a real blocker. Measure first; adapt after Phase 3
with explicit rationale and rollback criteria.

**What if leadership pressures for more simultaneous work?** Show impact projections: increasing WIP
tends to increase cycle time. Use current metrics to illustrate trade‑offs.

## Roles & Ownership

**What happens if someone picks a ticket beyond their current expertise?** Pair or micro‑swarm
early. Slower single ticket now accelerates future velocity via knowledge spread.

**How do senior engineers show growth?** Through architectural stewardship (design reviews), backlog
shaping, mentoring, quality bar leadership, and cross‑team influence recorded in design docs &
retros.

## Quality & Design Docs

**Aren’t design docs overhead for tiny changes?** Keep them proportional. Even a 5‑bullet doc for a
small change catches missing tests or existing abstractions to reuse.

**What if reviewers disagree?** Capture the options + trade‑offs succinctly in the doc; if consensus
still fails, timebox a focused huddle, then document the decision and reasoning.

**Why require two design AND two PR reviews?** Redundancy spreads knowledge, reduces blind spots,
and maintains consistency; small tickets keep review load reasonable.

## Metrics & Success

**How do we know it’s working?** Improvements in cycle time, reduced interrupt ratio, lower incident
frequency, broader Shepherd distribution, and positive pulse survey trends (`measuring-success.md`).

**What if metrics improve but morale drops?** Re‑examine WIP pressure, review load, and meeting
hygiene. Principle application may have become dogmatic; engage team in a Starfish Retro.

**Is velocity story point tracking needed?** No. Cycle time + throughput + quality metrics provide
richer insight; story points often devolve into negotiation games.

## Miscellaneous

**Can we use sprints?** You can, but Golazo does not require timeboxed iterations; continuous flow +
periodic planning typically yields smoother delivery.

**How do we manage external stakeholder asks?** Capture as backlog items, clarify acceptance
criteria, then WSJF rank. Avoid side channels creating invisible work.

## Still Have Questions?

Open an issue (include context + what you’ve already tried) or propose an addition via PR following
`contribution.md`.
