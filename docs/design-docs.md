# Design Docs

## Summary

Write down the approach before coding so peers can spot risks while it's still easy to change. Leave
enough detail for someone to understand why you made the decision later.

## Purpose and Benefits

- Give reviewers a chance to question the approach before you build it.
- Catch missing tests, tricky cases, and dependencies while you can still change the plan.
- Make it easier for pull request reviewers to focus on the code.
- Give future maintainers a record of what you decided and why.
- Show new contributors how the team has solved similar problems.
- Use the estimate and expected completion date to spot differences in what people think the ticket
  includes.

## Minimal Template

Copy the template from [Templates & Examples](templates.md).

1. Elevator Pitch
2. Definition of Done
3. Customer / Consumer
4. Dependencies and Assumptions
5. Design and Testing Approach
6. Task List
7. Estimated Completion
8. Signoffs
9. Implementation Notes

For a small ticket, a few bullets per section may be enough.

## Signoff Process

- The draft is ready for review when each section has initial content.
- Two peers review it and either sign off or ask for changes.
- Most clarifications should happen asynchronously, with the document updated as decisions change.
- Implementation normally starts after two signoffs.

Urgent Swarm work can be an exception. If the team often skips design review, look for decisions
that keep getting reopened in pull requests or problems that end up back in Swarm.

## During Implementation

- Keep the document current as important assumptions change.
- Add discoveries, data sources, and implementation notes that are likely to matter later.
- If the approach changes in a way that affects earlier decisions, pause and ask peers to review the
  design again before bringing it to the pull request.
- Record follow-up work explicitly instead of silently growing the current scope.

## Common Pitfalls and Avoidance

| Pitfall                           | Consequence                   | Mitigation                                    |
| --------------------------------- | ----------------------------- | --------------------------------------------- |
| Skipping docs for "small" changes | Hidden repeated rework        | Use a smaller doc instead of no doc           |
| Writing essays                    | Slow review and stale content | Prefer bullets, diagrams, and direct language |
| Signoff theater                   | False confidence              | Expect real questions, not just approval text |
| Letting drift accumulate          | Pull request surprises        | Update the doc when the approach changes      |

## Reviewer Checklist

- Does the definition of done include quality and validation expectations?
- Are important dependencies, risks, and assumptions visible?
- Does the design fit existing architecture and local patterns?
- Are there relevant existing tools, helpers, or prior decisions to reference?
- Is the work still small enough to fit the team SLA?
- Is the testing or monitoring plan explicit enough to evaluate?
- Are follow-up items clearly separated from current scope?

## Navigation

[← Step 5: Tickets](tickets.md) | [Step 7: Meetings →](meetings.md)
