# Why Golazo Works

## Summary

Golazo targets common sources of engineering drag: hidden rework, slow feedback loops, knowledge
silos, and operational noise. By constraining WIP and insisting on early shared understanding, it
accelerates value delivery while improving quality and morale.

## Problem → Mechanism → Outcome

| Problem Symptom                            | Golazo Mechanism                                     | Expected Outcome                                      |
| ------------------------------------------ | ---------------------------------------------------- | ----------------------------------------------------- |
| PR churn over fundamental design questions | Pre‑implementation design doc + 2 signoffs           | Smaller PRs focused on details; faster merges         |
| Large bug / incident backlog               | Immediate triage + Swarm rail + build quality in     | Lower incoming defect rate; faster resolution         |
| Rigid semester planning blocking new asks  | Frequent WSJF planning; small ticket slices          | Adaptable backlog; opportunity capture                |
| Overloaded on‑call / DRI                   | Upstream quality + rotation + automation focus       | DRI time shrinks; less burnout                        |
| Slow or absent reviews                     | Visible Review channel + limited WIP + small tickets | Predictable review latency                            |
| Isolation & silos                          | Anyone can pick any Ready ticket; shared design docs | Broader knowledge distribution                        |
| Slow new‑hire ramp                         | Pairing + reading past design docs + small tickets   | Confidence from first contribution in days not months |
| Single point of failure expertise          | Encourage workstream rotation                        | Reduced key‑person risk                               |
| Multitasking & overload                    | Strict individual & column WIP limits                | Focused flow; lower context switching                 |
| Large prolonged failed efforts             | Tickets capped by SLA + early validation             | Fail fast; low sunk cost                              |
| Low engagement / boredom                   | Autonomy to select next tickets                      | Higher motivation & retention                         |
| Lack of ownership                          | Team success framing + shared reviews & signoffs     | Collective accountability & pride                     |

## Key Challenges Explained

### Pull Request Churn

Without upfront alignment, PRs become the venue for architectural debates. Golazo shifts those
discussions earlier, reducing rewrite cycles.

### Incident & Bug Backlog

Every defect takes one of two paths: fix now (Swarm) or consciously defer after we decide the impact
doesn’t justify the fix. Quality practices (tests, monitoring, clear design) reduce how many arrive
in the first place. If there are high incoming rates, that is a flag for the team to pause to
investigate the cause whether technical or procedural.

### Planning Rigidity

Interruptions and plan changes are inevitable. WSJF plus short tickets means new high‑value work can
enter the flow within days—not semesters—without derailing existing commitments.

### DRI Overload

Because quality is built in and workstreams are shared, the DRI role becomes lightweight triage, not
perpetual firefighting. Automation and documentation improvements compound.

### Review Latency

Smaller, well‑scoped changes + explicit review signaling reduce the psychological barrier to jumping
into a review. Reviewers can quickly gain needed context via the design document that accompanies
the task.

### Knowledge Silos & Ramp

Rotational picking of diverse tickets along with living design doc archive distribute context. New
engineers learn by doing, not by prolonged observation and reading endless documentation.

### Focus & Multitasking Stress

WIP limits and right‑to‑left standup focus the team on finishing. Context switching declines;
predictable throughput rises.

### Large Initiative Risk

Decomposing into validated slices ensures feasibility and value checkpoints. Weak approaches are
discovered after days, not months.

### Motivation & Ownership

Autonomy in ticket selection together with collaborative completion fosters intrinsic motivation;
success is shared, not isolated.

## How Do We Know It’s Working?

The task board makes it visually obvious when work isn't flowing as expected, and, depending on the
board technology used, metrics can be calculated automatically. Practically speaking, Golazo teams
have happier team members, better teammate relationships, fewer surprise incidents, faster validated
releases, and onboarding speed improvements.

## Influences

Golazo synthesizes ideas from Lean (flow efficiency, waste reduction), Kanban (visualization, WIP
limits), and Agile (iterative delivery, feedback loops) while emphasizing lightweight documentation
as a knowledge engine. It is intentionally minimal. Each practice survives only if it demonstrably
improves flow and learning.

## Related

- Adoption Guide → [Adoption Guide](adoption-guide.md)
- Principles → [Principles & Mindset](principles.md)
