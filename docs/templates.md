# Templates and Examples

> Status: Scaffold — provide copy/paste starting points.

## Design Doc Template (Markdown)

```
# Title

## Elevator Pitch
(What value, for whom, why now)

## Definition of Done
- [ ] (TODO)

## Customer / Consumer
(TODO)

## Dependencies
- (TODO)

## Assumptions / Out of Scope
- (TODO)

## Design and Testing Approach
(TODO)

## Task List
- [ ] Implementation
- [ ] Tests
- [ ] Monitoring / Metrics
- [ ] Documentation

## Estimated Completion (95% Confidence)
(TODO: YYYY-MM-DD)

## Signoffs
- Reviewer 1: (Name / Date)
- Reviewer 2: (Name / Date)

## Implementation Notes
(TODO)
```

## Ticket Sizing Checklist

Use before pulling a ticket from Ready or when splitting.

- Delivers standalone, demonstrable value (stakeholder can say ✅ / ❌).
- Fits within SLA (less than 2 weeks, ideally a few days).
- Acceptance criteria are concrete and testable.
- Quality signals (tests, monitoring, docs) identified.
- Design complexity understood or a spike precedes it.
- Dependencies known and minimal; external waiting minimized.
- Can be shepherded by a single person (pairing allowed) without blocking others.

## Retro Action Item Format

```
Action: <description>
Owner: <name>
Due: <date>
Success Signal: <metric or observable change>
```

## Review Status Emojis (Accessible)

State should always be mirrored with short text for assistive tech:

- :eyes: Reviewing ("@channel Reviewing – expect feedback in ~30m")
- :speech_balloon: Feedback posted ("Comments added; awaiting responses")
- :thumbsup: Approved ("Second approval complete; ready to merge")

Optional: :hourglass_flowing_sand: Waiting on external dependency / data.

## Related

- Design Docs - [Design Docs](design-docs.md)
- Communication - [Communication Patterns](communication.md)
