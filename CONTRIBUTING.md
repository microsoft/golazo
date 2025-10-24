# Contributing to Golazo

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit
[https://cla.opensource.microsoft.com](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide a
CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the
[Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more
information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact <opencode@microsoft.com> with any additional questions or comments.

## Development Environment

You can contribute to this project from a macOS, Linux or Windows machine.

On all platforms, the minimum requirements are:

- Git client and command line tools

## Pull Requests

### How to create pull requests

To create a new PR, fork the project on GitHub and clone the upstream repo:

```sh
git clone https://github.com/Microsoft/golazo.git
```

Navigate to the repo root:

```sh
cd golazo
```

Add your fork as an origin:

```sh
git remote add fork https://github.com/YOUR_GITHUB_USERNAME/golazo.git
```

Check out a new branch, make modifications, and push the branch to your fork:

```sh
$ git checkout -b feature
# edit files
$ git commit
$ git push fork feature
```

Open a pull request against the main `golazo` repo.

#### Tips and best practices for pull requests

- If the PR is not ready for review, please mark it as
  [`draft`](https://github.blog/2019-02-14-introducing-draft-pull-requests/).
- Submit small, focused PRs addressing a single concern/issue.
- Make sure the PR title reflects the contribution.
- Write a summary that helps understand the change.
- Include usage examples in the summary, where applicable.

### How to get pull requests merged

A PR is considered to be **ready to merge** when:

- Major feedback/comments are resolved.
- It has been open for review for at least one working day. This gives people reasonable time to
  review.
- Approved by at least one code owner.

### When to start with a Discussion or Issue

Much of the Golazo documentation is subjective and prescriptive by nature. Since teams may have
differing opinions on processes and practices, we encourage open discussion before making
substantial changes.

**Submit a PR directly for:**

- Obvious corrections (broken links, typos, misspellings)
- Formatting improvements
- Adding missing documentation
- Clarifying existing content

**Start with a GitHub Discussion or Issue for:**

- Changes to recommended processes or practices
- Adding or removing workflow steps
- Modifying prescriptive guidance
- Significant restructuring of content
- Topics where reasonable people might disagree

This approach aligns with the spirit of Golazo itself: **discuss the plan before doing the work**.
Starting with a discussion helps build consensus, avoids unnecessary rework, and ensures changes
reflect the community's needs.

Of course, you're always welcome to submit a PR for any change, but be prepared that process-related
changes may require more discussion and iteration.

## Symbol Usage

### Use Words Instead of Symbols

**Do not use mathematical or symbolic operators in prose text or lists.** These symbols can be
confusing, inaccessible to screen readers, and may not translate well across different contexts.

#### Arrow Symbol (→)

❌ **Don't:**

- "Move from Backlog → Ready"
- "Adoption Guide → [Adoption Guide](adoption-guide.md)"
- "Small changes → faster reviews"

✅ **Do:**

- "Move from Backlog to Ready"
- "Adoption Guide - [Adoption Guide](adoption-guide.md)"
- "Small changes then faster reviews" (when indicating consequence)

#### Plus Symbol (+)

❌ **Don't:**

- "Design docs + 2 signoffs"
- "Tests + monitoring + documentation"
- "Q&A"

✅ **Do:**

- "Design docs and 2 signoffs"
- "Tests, monitoring, and documentation"
- "Q and A" or "Questions and Answers"

#### Greater Than or Equal (≥)

❌ **Don't:**

- "≥2 peer signoffs"
- "Access to coach (≥ first 4 weeks)"

✅ **Do:**

- "2 or more peer signoffs"
- "at least 2 peer signoffs"
- "Access to coach (at least first 4 weeks)"

#### Less Than or Equal (≤)

❌ **Don't:**

- "≤2 active tickets"
- "≤ 30% of capacity"

✅ **Do:**

- "2 or fewer active tickets"
- "at most 2 active tickets"
- "no more than 30% of capacity"

#### Less Than (<)

❌ **Don't:**

- "< 2 weeks"
- "tickets < 5 days"

✅ **Do:**

- "less than 2 weeks"
- "under 2 weeks"
- "tickets under 5 days"

#### Ampersand (&)

❌ **Don't:**

- "Meetings & Cadence"
- "WIP limits & highlight bottlenecks"
- "Dependencies & Assumptions"

✅ **Do:**

- "Meetings and Cadence"
- "WIP limits and highlight bottlenecks"
- "Dependencies and Assumptions"

### Exceptions

Symbols **may** be used in the following contexts:

1. **Headers and Titles** - If established as a proper name (e.g., "WIP & Flow" as a page title)
2. **Tables** - Column headers or data cells where space is constrained
3. **Code snippets** - Programming syntax and examples
4. **Formulas** - Mathematical expressions (e.g.,
   `WSJF = (Cost of Delay + Business Value) / Effort`)
5. **HTML entities** - When using `&nbsp;` or similar for formatting

## Writing Style

### Be Clear and Concise

- Use short sentences when possible
- Prefer active voice: "The team reviews" over "The review is done by the team"
- Avoid jargon without explanation

### Use Consistent Terminology

- Refer to the [Glossary](glossary.md) for canonical terms
- Use the same term consistently throughout (e.g., don't alternate between "ticket" and "work item")

### Be Inclusive and Accessible

- Write for screen readers: avoid relying solely on formatting or symbols
- Use descriptive link text: "See [Adoption Guide](adoption-guide.md)" not "Click
  [here](adoption-guide.md)"
- Provide alt text for images and diagrams when they are added

### Structure for Scanning

- Use descriptive headers
- Break up long paragraphs
- Use bulleted lists for multiple items
- Use numbered lists for sequential steps

## Markdown Formatting

### Headers

Use ATX-style headers (`#`) with proper hierarchy:

```markdown
# Page Title (H1 - only one per page)

## Major Section (H2)

### Subsection (H3)

#### Minor Section (H4)
```

### Lists

Unordered lists should use `-` (hyphen):

```markdown
- First item
- Second item
- Third item
```

Ordered lists should use numbers:

```markdown
1. First step
2. Second step
3. Third step
```

### Links

Use reference-style links for cross-references:

```markdown
See [Related Page](related-page.md) for more details.
```

Not:

```markdown
See [Related Page](../docs/related-page.md)
```

### Code and Commands

Inline code uses single backticks:

```markdown
The `Coach` role facilitates standup.
```

Code blocks use triple backticks with language identifier:

````markdown
```python
def example():
    return "Hello"
```
````

### Emphasis

- Use **bold** for key concepts or strong emphasis
- Use _italics_ for subtle emphasis or terms being defined
- Use `code formatting` for technical terms, file names, and commands

## Tables

### Keep Tables Simple

- Avoid overly wide tables
- Consider breaking complex tables into multiple simpler ones
- Ensure tables work well on mobile devices

### Table Formatting

Use consistent alignment:

```markdown
| Column 1     | Column 2               | Column 3     |
| ------------ | ---------------------- | ------------ |
| Left-aligned | Also left-aligned      | Data         |
| More data    | Additional information | More content |
```

## Document Structure

### Every Page Should Have

1. **Title** - Clear H1 at the top
2. **Status/Context Note** (if applicable) - Draft status, dependencies
3. **Summary Section** - 2-3 sentence overview
4. **Body Content** - Main sections with clear headers
5. **Related Section** - Links to connected pages

### Example Template

```markdown
# Page Title

> Status note (if applicable)

## Summary

Brief overview of what this page covers and why it matters.

## Main Section

Content here...

### Subsection

More details...

## Related

- [Related Page 1](page1.md)
- [Related Page 2](page2.md)
```
