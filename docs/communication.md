# Communication Patterns

> Public draft – adapted from legacy FAQ + Asynchronous Communication guidance.

## Summary

Intentional, transparent communication keeps flow moving across time zones and schedules. Favor
written, searchable, lightweight artifacts over private chats and meetings.

## Principles

- **Default to Public** – Use shared team channels so others can learn passively.
- **Context over Pings** – Provide enough detail so someone returning later can answer without a
  back‑and‑forth.
- **Async Friendly** – Assume recipients may respond hours later; batch questions.
- **Signal Review States** – Make design / PR status legible at a glance.
- **Avoid Notification Fatigue** – High‑signal channels only; thread conversations.

## Recommended Channels (Tool Agnostic)

| Channel              | Purpose                                             | Notes                                        |
| -------------------- | --------------------------------------------------- | -------------------------------------------- |
| Dev General          | Everyday technical discussion, questions, decisions | Prefer here over 1:1 DMs for discoverability |
| Review               | Each design doc & PR gets a thread                  | Status signaled via emoji + short text       |
| Release              | Deployment coordination & approvals                 | Include links + expected impact summary      |
| Social               | Non‑work bonding & quick availability notes         | Optional notifications                       |
| (Optional) Incidents | High‑noise real‑time response (if volume justifies) | Summarize resolution in ticket after         |

## Review Signaling

Use both emoji and short text for accessibility (screen readers may not convey intent):

- :eyes: "Reviewing" – Someone actively reading.
- :speech_balloon: "Comments posted" – Feedback awaiting author response.
- :thumbsup: "Approved" – Signoff given. If stale > a few hours, politely re‑ping or tag a likely
  reviewer.

## Async Best Practices

| Instead of                   | Prefer                                                  |
| ---------------------------- | ------------------------------------------------------- |
| "hi" (wait)                  | Immediate full question + context                       |
| Private DM for general issue | Public channel for shared learning                      |
| Vague bug report             | Steps, expected vs actual, logs, environment            |
| Large design debate in chat  | Summarize options in design doc; request focused review |
| Unstructured status update   | Board + concise delta notes                             |

When asking: include links (ticket, PR, logs), reproduction steps, and what you’ve already tried.

## Onboarding Communication

Week 1 guidance for newcomers:

- Lurk in Dev General to absorb norms; upgrade to asking clarifying questions by day 2–3.
- Shadow one review thread end‑to‑end.
- Post a first design doc or PR thread with explicit request: “Looking for two reviewers; focusing
  on X risk.”
- Practice writing a full context question instead of a DM; get feedback from Coach.

## Healthy Information Radiators

- Board columns & WIP limits (current flow state).
- Design docs (approach & rationale).
- Review channel threads (work needing attention).
- Metrics dashboard (trend insights, not immediate alerts).

## Anti‑Patterns

- Important decisions only in meetings (no written record).
- DM reliance creating knowledge silos.
- Review threads with only emoji (no explanatory text for later readers).
- Channel sprawl: too many low‑usage channels diluting attention.

## Related

- Design Docs → [Design Docs](design-docs.md)
- Meetings → [Meetings & Cadence](meetings-and-ceremonies.md)
- Templates → [Templates & Examples](templates.md)
