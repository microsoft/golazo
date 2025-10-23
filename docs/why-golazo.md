# Why Golazo Works

> Public draft – converts legacy "You Might Need Golazo If..." list into problem→mechanism→outcome
> mapping.

## Summary

Golazo targets common sources of engineering drag: hidden rework, slow feedback loops, knowledge
silos, and operational noise. By constraining WIP and insisting on early shared understanding, it
accelerates value delivery while improving quality and morale.

## Problem → Mechanism → Outcome Matrix

| Problem Symptom                            | Golazo Mechanism                                                | Expected Outcome                                  |
| ------------------------------------------ | --------------------------------------------------------------- | ------------------------------------------------- |
| PR churn over fundamental design questions | Pre‑implementation design doc + 2 signoffs                      | Smaller PRs focused on details; faster merges     |
| Large bug / incident backlog               | Immediate triage + Swarm rail + build quality in                | Lower incoming defect rate; faster resolution     |
| Rigid semester planning blocking new asks  | Frequent WSJF planning; small ticket slices                     | Adaptable backlog; opportunity capture            |
| Overloaded on‑call / DRI                   | Upstream quality + rotation + automation focus                  | DRI time shrinks; less burnout                    |
| Slow or absent reviews                     | Visible Review channel + limited WIP + small tickets            | Predictable review latency                        |
| Isolation & silos                          | Anyone can pick any Ready ticket; shared design docs            | Broader knowledge distribution                    |
| Slow new‑hire ramp                         | Pairing + reading past design docs + small tickets              | First contribution confidence in weeks not months |
| Single point of failure expertise          | Encourage color (workstream) rotation; track Shepherd diversity | Reduced key‑person risk                           |
| Multitasking & overload                    | Strict individual & column WIP limits                           | Focused flow; lower context switching             |
| Uncertain efficiency / direction           | Metrics dashboard + retros + VSM                                | Data‑informed improvements                        |
| Large prolonged failed efforts             | Tickets capped by SLA + early validation                        | Kill weak ideas early; low sunk cost              |
| Low engagement / boredom                   | Autonomy to select next tickets; learning rotation              | Higher motivation & retention                     |
| Lack of ownership feeling                  | Team success framing + shared reviews & signoffs                | Collective accountability & pride                 |

## Key Challenges Explained

### Pull Request Churn

Without upfront alignment, PRs become the venue for architectural debates. Golazo shifts those
discussions earlier, reducing rewrite cycles.

### Incident & Bug Backlog

Defects are either fixed immediately (Swarm) or consciously accepted. Quality practices (tests,
monitoring, design clarity) curb future inflow.

### Planning Rigidity

WSJF plus short tickets means new high‑value work can enter the flow within days—not
semesters—without derailing existing commitments.

### DRI Overload

Because quality is built in, the DRI role becomes lightweight triage, not perpetual firefighting.
Automation and documentation improvements compound.

### Review Latency

Smaller, well‑scoped changes + explicit review signaling reduce the psychological barrier to jumping
into a review.

### Knowledge Silos & Ramp

Rotational picking of diverse tickets + living design doc archive distribute context. New engineers
learn by doing, not by prolonged observation.

### Focus & Multitasking Stress

WIP limits and right‑to‑left standup focus the team on finishing. Context switching declines;
predictable throughput rises.

### Large Initiative Risk

Decomposing into validated slices ensures feasibility and value checkpoints. Weak approaches are
discovered after days, not months.

### Motivation & Ownership

Autonomy in ticket selection + collaborative completion fosters intrinsic motivation; success is
shared, not isolated.

## How Do We Know It’s Working?

See `measuring-success.md` for metrics. Practically: happier team members, fewer surprise incidents,
faster validated releases, and onboarding speed improvements. If metrics improve but morale tanks,
reassess execution (principles may be applied mechanically rather than thoughtfully).

## Related

- Measuring Success → `measuring-success.md`
- Adoption Guide → `adoption-guide.md`
- Principles → `principles.md`
