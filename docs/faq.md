# Frequently Asked Questions

## Team Operation

**How big should a team be?** Golazo tends to work best with roughly 6 to 8 engineers. That is
usually enough diversity for pairing and review without losing shared context. Larger groups can use
multiple boards with explicit coordination between leads or coaches.

**Can a single engineer use Golazo practices?** Yes, at least in part. A single engineer can still
use small tickets, lightweight design notes, personal WIP limits, and explicit review requests. Some
of the benefits are smaller without a team, but the discipline can still be useful.

**What if a ticket stalls?** Raise it in standup immediately. If it continues to age, inspect it as
an outlier. Common causes include hidden dependencies, oversized scope, unclear validation, and
review delays.

## Adoption and Transition

**How long is the trial?** Usually about 90 days. That is long enough for the team to experience the
process under more than one planning cycle and to see whether early costs are offset by lower churn.

**Do we customize Golazo early?** Usually no. Change it only when there is a real blocker and the
reason is explicit. Early customization often removes the parts that make the system internally
coherent.

**What if leadership pressures for more simultaneous work?** Show the tradeoff directly. Higher WIP
usually means longer cycle time and more partial work. If the business needs more work in flight,
the team should make that cost visible rather than quietly absorbing it.

## Roles and Ownership

**What happens if someone picks a ticket beyond their current expertise?** That is usually good for
the team, provided they pair early enough and ask for review before the work gets too far ahead.
Short-term slowdown can be a rational trade for broader long-term capability.

**How do senior engineers show growth?** Through shaping work, reviewing design, mentoring,
improving system quality, and influencing how the team operates across boundaries. Golazo does not
remove senior scope. It changes the artifacts through which that scope becomes visible.

## Quality and Design Docs

**Aren't design docs overhead for tiny changes?** They should be proportional. For genuinely small
changes, a few bullets may be enough. The point is to externalize the key assumptions, not to force
full prose.

**What if reviewers disagree?** Capture the options and tradeoffs in the design doc, then resolve
the decision in a focused follow-up conversation if needed. After that, update the document so the
outcome is visible to later readers.

**Why require two design and two PR reviews?** The redundancy helps spread knowledge and catch blind
spots. The requirement is easier to sustain when tickets stay small.

## Metrics and Success

**How do we know it’s working?** Look for directionally healthier signals: lower cycle time, fewer
interrupts overwhelming planned work, fewer incidents, broader ownership across workstreams, and a
team that is less dependent on private context.

**What if metrics improve but morale drops?** That suggests the team may be optimizing the visible
numbers while ignoring workload, review burden, or meeting quality. In that case, inspect the system
again rather than assuming the process is working simply because one metric improved.

**Is velocity or story point tracking required?** No. Throughput, cycle time, review delay, and
quality signals usually provide more useful insight.

## Miscellaneous

**Can we use sprints?** Yes, but Golazo does not depend on timeboxed delivery. Continuous flow with
periodic planning is usually the simpler default.

**How do we manage external stakeholder asks?** Put them on the board, define acceptance criteria,
and prioritize them with the rest of the work. Side channels create invisible work and make the
system harder to trust.

## Still Have Questions?

Open a GitHub issue or discussion with enough context to explain what you are trying to do and where
the current guidance is unclear.

## Navigation

[← Step 10: Adoption Guide](adoption-guide.md)
