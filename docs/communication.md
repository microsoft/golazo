# Communication Patterns

## Summary

Intentional, transparent communication keeps flow moving across time zones and schedules. Golazo
favors written, searchable, lightweight asynchronous artifacts over private chats and meetings.

## Principles

- Default to Public Conversation: Use shared team channels so others can learn passively.
- Context over Pings: Provide enough detail so someone returning later can answer without a
  back‑and‑forth.
- Async Friendly: Assume recipients may respond hours later; batch questions.
- Signal Review States: Make design / PR status legible at a glance.
- Avoid Notification Fatigue: Thread conversations and avoid tagging the entire channel.

## Recommended Channels

| Channel     | Purpose                                             | Notes                                        |
| ----------- | --------------------------------------------------- | -------------------------------------------- |
| Dev General | Everyday technical discussion, questions, decisions | Prefer here over 1:1 DMs for discoverability |
| Review      | Each design doc and PR gets a thread                | Status signaled via emoji and short text     |
| Release     | Deployment coordination and approvals               | Include links and expected impact summary    |
| Social      | Non‑work bonding and quick availability notes       | Encourage fun!                               |

## Review and Release Signaling

Define a team culture around communicating status of reaction to posts in the Review and Release
channels. For example, the team could use common emojis:

- :eyes: "Reviewing" – Someone actively reading.
- :speech_balloon: "Comments posted" – Feedback awaiting author response.
- :thumbsup: "Approved" – Signoff given. If stale for more than a few hours, politely re‑ping or tag
  a likely reviewer.

## Async Best Practices

| Instead of                   | Prefer                                                  |
| ---------------------------- | ------------------------------------------------------- |
| "hi" (wait)                  | Immediate full question and context                     |
| Private DM for general issue | Public channel for shared learning                      |
| Vague bug report             | Steps, expected vs actual, logs, environment            |
| Large design debate in chat  | Summarize options in design doc; request focused review |
| Unstructured status update   | Board and concise delta notes                           |

When asking: include links (ticket, PR, logs), reproduction steps, and what you’ve already tried.

## Anti‑Patterns

- Important decisions only in meetings with no written record.
- Direct message reliance creating knowledge silos.
- Too many low‑usage channels diluting attention.

## Related Links

[← Step 8: WIP & Flow](wip-and-flow.md) | [Step 10: Adoption Guide →](adoption-guide.md)

- Design Docs - [Design Docs](design-docs.md)
- Meetings - [Meetings](meetings.md)
- Templates - [Templates & Examples](templates.md)
