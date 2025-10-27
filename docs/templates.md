# Templates and Examples

## Design Doc Template

```
# Title

## Elevator Pitch
(What value, for whom, why now)
TODO

## Definition of Done
(Bulleted list describing the exit criteria and desired end state. Should be clear how success is determined and measured)
- TODO

## Customer / Consumer
(Who will be consuming this work? Who will validate that it is correct?)
- TODO

## Dependencies
(Key/major people or technology)
- TODO

## Assumptions / Out of Scope
(Assumptions when planning the ticket and/or related work that is not in scope for this ticket)
- TODO

## Design and Testing Approach
(Free text/diagram/picture/etc that clearly shows your approach and considerations)
- TODO

## Task List
(Bulleted list of engineering work, documentation, monitors, TSGs, etc. Engineering will be complete when the list is finished.)
- [ ] Implementation
- [ ] Tests
- [ ] Monitoring / Metrics
- [ ] Documentation

## Estimated Completion
(You have 95% confidence that teh work will be completed by this date barring any enormous disaster.)
- YYYY-MM-DD

## Signoffs
- Reviewer 1: (Name / Date)
- Reviewer 2: (Name / Date)

## Implementation Notes
(Optional place to include key learnings, decisions, discoveries, data sources, contact information, etc)
TODO
```

## Ticket Sizing Checklist

Use before pulling a ticket from Ready or when splitting.

- Delivers standalone, demonstrable value (stakeholder can say ✅ / ❌).
- Fits within SLA (less than 2 weeks, ideally a few days).
- Acceptance criteria are concrete and testable.
- Quality signals (tests, monitoring, docs) identified.
- Design complexity understood or a spike precedes it.
- Dependencies known and minimal; external waiting minimized.
- Can be shepherded by a single person (pairing allowed) without being blocked on others.
