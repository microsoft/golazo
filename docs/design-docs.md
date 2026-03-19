# Design Docs

## Summary

Golazo uses short design documents to align on approach before implementation. The goal is not to
produce formal specification documents. The goal is to reduce avoidable rework, surface risks while
changes are still cheap, and leave behind enough context that future readers can understand why a
decision was made.

Design docs work best when they are short, specific, and current.

## Purpose and Benefits

- Shared Context Before Code: reviewers can react to the intended approach before implementation is
  expensive to change.
- Higher Quality Implementation: edge cases, dependencies, and testing concerns are more likely to
  be noticed early.
- Faster Reviews: pull requests can focus more on execution details and less on first-principles
  design debate.
- Knowledge Base: future maintainers can reconstruct reasoning without relying on memory.
- Onboarding Support: new contributors can read earlier docs to understand local patterns.
- Predictability: early sizing and an estimated completion date can expose mismatched assumptions.

The benefit is usually cumulative rather than dramatic on any single ticket.

## Minimal Template

Keep the template lean. Optimize for clarity rather than polish. A copyable version lives in
[Templates & Examples](templates.md).

1. Elevator Pitch
2. Definition of Done
3. Customer / Consumer
4. Dependencies and Assumptions
5. Design and Testing Approach
6. Task List
7. Estimated Completion
8. Signoffs
9. Implementation Notes

That is enough structure for most tickets. If the work is genuinely small, each section may only
need a few bullets.

## Signoff Process

- The draft is ready for review when each section has initial content.
- Two peers review it and either sign off or ask for changes.
- Most clarifications should happen asynchronously, with the document updated as decisions change.
- Implementation normally starts after two signoffs.

There are exceptions for urgent swarm work, but those should remain exceptions. If the team skips
design review frequently, it should expect more swarms and pull request churn later.

## During Implementation

- Keep the document current as important assumptions change.
- Add discoveries, data sources, and implementation notes that are likely to matter later.
- If the design changes materially, pause and re-review rather than letting the pull request become
  the place where the new design is first introduced.
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
