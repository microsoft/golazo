# Communication Patterns

## Summary

Golazo assumes teams will often work asynchronously, even when they sit in the same office. That is
why communication defaults toward written, searchable, shared artifacts instead of private messages
or meetings. It is a practical preference for communication that smoothly handles time zones,
interruptions, and staff changes.

## Principles

- Default to Public Conversation: use shared channels unless there is a real reason not to.
- Context Over Pings: ask the full question up front rather than creating an extra round trip.
- Async Friendly: assume the reader may respond later and give them enough information to do so.
- Signal Review States: make review and release status visible without requiring follow-up messages.
- Avoid Notification Fatigue: thread conversations and avoid broad tagging when a narrower audience
  is enough.

## Recommended Channels

| Channel     | Purpose                                             | Notes                                       |
| ----------- | --------------------------------------------------- | ------------------------------------------- |
| Dev General | Everyday technical discussion, questions, decisions | Prefer this over private DMs for shared use |
| Review      | Threads for design docs and pull requests           | Keep review state visible                   |
| Release     | Deployment coordination and release approval        | Include links and expected impact           |
| Social      | Non-work interaction and light coordination         | Useful, but separate from operational noise |

The names may vary by team. The underlying separation is what matters.

## Review and Release Signaling

Teams should define a small, consistent set of signals in review and release channels. For example:

- 👀 means someone is actively reviewing
- 💬 means comments are posted and a response is needed
- 👍 means approval is given

Consistency is more important than the exact symbols. The goal is to make the state of reviews and
releases quickly scannable.

## Async Best Practices

| Instead of                     | Prefer                                                                           |
| ------------------------------ | -------------------------------------------------------------------------------- |
| "hi" and then waiting          | Ask the actual question with enough context to answer it                         |
| Private DM for a general issue | A shared channel where others can benefit and contribute                         |
| Vague bug report               | Reproduction steps, expected and actual behavior, logs, and environment details  |
| Long design debate in chat     | A short summary in the design doc plus a focused review request                  |
| Unstructured status update     | What was learned, what is blocked, and what is needed to move the ticket forward |

When asking for help, include links to the relevant ticket, pull request, logs, or dashboard, plus
what you already tried.

## Anti‑Patterns

- Making important decisions only in meetings with no written follow-up
- Relying on direct messages for issues that affect the broader team
- Creating so many channels that attention fragments and none stay healthy

## Navigation

[← Step 8: WIP & Flow](wip-and-flow.md) | [Step 10: Adoption Guide →](adoption-guide.md)
