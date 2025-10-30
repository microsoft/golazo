# Golazo Overview Video Plan (≈10 Minutes)

Purpose: Provide new external engineers a fast mental model of Golazo—why it exists, the pains it
eliminates, and how core practices (design docs, task board, WIP limits, validation) interlock to
produce predictable, low‑friction delivery. Audience: Skeptical/pragmatic engineers & tech leads
(small–mid teams, 4–10 engineers) evaluating lightweight process improvements. Tone: Empathetic,
concise, anti‑ceremony, outcome‑focused. Exclusions: Deep WSJF math, meeting minutiae, exhaustive
ticket taxonomy.

---

## Segment Outline & Timing

### 0:00–0:45 Opening Hook & Credibility

- Talking head: Brief rapid verbal list of pains (slow reviews, surprise rework, Slack pings,
  context switching, fragile ownership, "Done = merged").
- Cut to single screen capture (slide or doc) with the 6 pain bullets; simple fade in.
- Tagline text: Less friction · Faster flow · Real validation.
- Goal: Establish relevance; viewers feel "This is our world."

### 0:45–2:00 What Is Golazo (Definition + Pillars)

- Definition: Lightweight engineering methodology optimizing flow, shared understanding, and
  customer validation.
- Pillars (high-level list): small value-sliced tickets; tiny collaborative design docs (2
  signoffs); visual task board w/ priority rails; WIP limits & swarm response; explicit validation
  stage.
- Visual: Sequential screen captures: (1) Sample mini design doc template (header + sections) then
  (2) Task board columns (high-level) while narrator describes flow.

### 2:00–3:00 Friction → Practice Mapping

| Pain                  | Golazo Response                             |
| --------------------- | ------------------------------------------- |
| Rework in reviews     | Upfront collaborative mini design docs      |
| Slow feedback loops   | Small batch tickets + visible flow board    |
| Knowledge silos       | Anyone can pull Ready tickets + pairing     |
| Multitasking overload | WIP limits enforce focus                    |
| Fragile ownership     | Shared pool + searchable design doc library |
| "Done" mismatch       | Customer validation stage                   |

- Goal: Show intentional, non-ceremonial targeting of issues.
- Visual: Static table (markdown rendered or slide). Optional subtle highlight box as each row is
  referenced (can be done via cursor hover or simple editing jump cut).

### 3:00–4:00 Design Docs (Core Mechanism)

- Characteristics: ~5–10 min write; concise (Context, Goal, Constraints, Open Questions, Validation
  Plan).
- Process: Draft stub → async clarification → 2 signoffs → implementation.
- Benefits: Early alignment, risk surfacing, reusable searchable context, supports AI assistants.
- Visual: Live scroll through a real (sanitized) mini design doc in editor; use cursor circles or
  brief zoom on key sections (Context, Open Questions, Validation Plan). No custom graphics.

### 4:00–5:10 Task Board & Priority Rails

- Columns (example set): Ideas · Drafting · Design Review · Ready · In Progress · Review ·
  Validation · Done.
- Rails: Swarm (urgent collaborative), Interrupt (reactive/support), Planned (normal flow).
- Pull model: Engineers self-select any Ready ticket → spreads knowledge, reduces queueing.
- Visual: Two or three static captures of the board at different stages of a single ticket (Design
  Review → Ready → In Progress → Review → Validation → Done). Simple rectangle highlight added in
  post (or cursor hover). Rails indicated by colored labels in the capture; no animation needed.

### 5:10–6:10 WIP Limits & Flow

- Why: Reduce context switching, speed completion, enable rapid incident swarm.
- Mechanics: Caps per engineer/team on In Progress + Review items; breach triggers unblock/swap.
- Visual: Side-by-side screen captures: (Left) board with many simultaneously In Progress items
  (mock overload); (Right) cleaned board with few active items. Optional text overlay: "High WIP" /
  "Low WIP".
- Goal: Internalize "Less started = more finished."

### 6:10–7:00 Small Tickets & Slicing

- Heuristics: Clear user value; ≤1–2 days; explicit validation plan; linked design doc.
- Approach: Slice by value/learning increments, not layers.
- Visual: Single screen (slide or doc) listing a feature and 4–5 small slice bullet points with
  brief validation notes. Fade between full feature vs sliced list.
- Benefit: Faster feedback, lower integration risk.

### 7:00–7:45 Integrated Review & Knowledge Spread

- Shift: Architectural debate moved earlier → Reviews focus on implementation quality.
- Practices: Pairing & rotation; reading past design docs accelerates ramp.
- Outcome: Lean, surgical PR comments; broader domain literacy.
- Visual: Show a small PR diff (screen capture) with concise comments. Contrast (optional) by
  briefly flashing a mock large diff screenshot (static) labeled "Before" then main focused diff
  "After".

### 7:45–8:30 Customer Validation Stage

- Definition of Done: Observed value (usage metrics, stakeholder confirmation, pilot feedback,
  dogfooding).
- Loop: Failed validation re-enters board (visible learning, not hidden churn).
- Visual: Board capture showing ticket in Validation column; then next capture with ticket moved to
  Done and a small text overlay "Value Observed". Simple crossfade.

### 8:30–9:15 Adoption Path (Layered Rollout)

1. Start: Shared board + mini design docs.
2. Add WIP limits once board hygiene stable.
3. Introduce explicit validation criteria.
4. Tune priority rails; schedule pairing rotation.

- Pitfalls: Overscoping docs; ignoring WIP breaches; vague validation definitions.
- Visual: Numbered list on a single slide or doc; reveal steps via simple jump cuts (no animation).

### 9:15–9:40 Closing & Call to Action

- Recap mantra: Small · Visible · Collaborative · Validated.
- CTA: Read "Why Golazo" then try one ticket tomorrow with a mini design doc.
- Visual: Final slide with 4 bold words in a vertical list: Small / Visible / Collaborative /
  Validated. Talking head remains picture-in-picture.

---

## Production Notes (Cross-Cutting)

- Voice: Confident & empathetic ("We’ve all wrestled with...").
- On-screen aids: Keywords for each segment; simple tables/lists (no custom graphics); Pain →
  Practice table early.
- Accessibility: High-contrast text overlays; concise phrasing; avoid jargon w/o definition.
- Editing rhythm: Fast cuts in intro; calmer pacing for design docs & board.
- Asset needs (all simple screen captures):
  1. Mini design doc template (real markdown file).
  2. Task board at several progression states.
  3. Overloaded vs clean WIP board capture.
  4. Feature slicing bullet list doc.
  5. Small PR diff with concise comments.
  6. Validation vs Done board capture.
  7. Adoption steps numbered list.
  8. Markdown board mock (`board-mock.md`) for anonymized recording.
- Music: Light unobtrusive bed; optional subtle dip before key definitions. No need for sound design
  hits.

### Minimal Visual Implementation

- Format: Talking head (primary) + occasional full-screen capture; use picture-in-picture for
  board/design doc sections if tool supports.
- Tools: Basic screen recorder (OBS, Xbox Game Bar, or system recorder) at 1080p; markdown and board
  in high-contrast theme.
- Editing style: Hard cuts or simple crossfades; no motion graphics, no kinetic text.
- Overlays: If available, use simple semi-transparent rectangle highlight; else rely on cursor
  hover + verbal callout.
- Color reliance: Keep meaning conveyed even if viewed grayscale
- Accessibility: Ensure font size ≥ 16–18px equivalent; avoid cramped multi-column shots.
- Consistency: Same editor theme, same board zoom level throughout to reduce cognitive load.
- Backup plan: If board tooling hard to anonymize, recreate a simplified board in a markdown table.

## Optional Shorter Cuts

- 5-min Version: Merge segments 2–4
- 2-min Teaser: Hook + Pillars + CTA only.

## Next Steps

- Draft full narration script (~1,100–1,300 words) with visual cues.
- Create sample design doc artifact (MD + screenshot).
- Storyboard frames per segment.
- Gather brand palette & typography.

---

_Last updated: 2025-10-29 (visuals simplified for talking head + screen capture)_
