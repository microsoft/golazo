# Golazo Public Documentation Information Architecture

This document defines the proposed public-facing reorganization of the existing internal-focused
Golazo markdown found in `docs/old/`. It preserves all substantive information while making the
content:

- Accessible to any engineering audience (no company-specific jargon, email lists, or internal tool
  dependencies)
- Progressive in depth (skim first, then drill down)
- Modular (pages can stand alone when linked externally)
- Maintained (clear single-source for each concept to avoid drift)
- Outcome & reader question oriented (each page answers a set of concrete questions)

---

## Page Overview (Proposed New Structure)

| #   | New Page (filename)              | Working Title                           | Purpose / Focus                                                                    | Primary Audience              | Key Reader Questions                                       | Source Mapping (Old File → Sections)                                                                           | Rewrite / Sanitization Notes                                                                                              |
| --- | -------------------------------- | --------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 1   | `index.md`                       | Golazo: Lean Team Flow                  | Landing page; concise value proposition + navigation to Why, How, and Quick Start. | Evaluators, newcomers         | What is Golazo? Why should I care? Where do I go next?     | `old/index.md` (intro + Where To Start) + `fundamentals.md` (Quick Version) + `reasons.md` (intro)             | Remove internal phrasing; add 30–50 word pitch; external links only.                                                      |
| 2   | `why-golazo.md`                  | Why Golazo Works                        | Motivation & pain-point framing (formerly "You Might Need Golazo If…").            | Skeptical engineers, managers | Does this solve my problems? Which symptoms match my team? | `reasons.md` (all subsections) + FAQ: "How do we know if it's working?"                                        | Convert ellipsis headings to problem statements; add summary matrix at top; de-internalize metrics (no MSPoll specifics). |
| 3   | `principles.md`                  | Principles & Mindset                    | Core lean / flow principles underpinning mechanics.                                | All                           | What philosophy drives the rules?                          | `fundamentals.md` → Principles list                                                                            | Add brief origin note (generic) not tied to company teams.                                                                |
| 4   | `roles.md`                       | Roles & Responsibilities                | Define Coach & DRI plus optional roles; ownership expectations.                    | Team members & leads          | Who does what? How do rotations work?                      | `fundamentals.md` → Roles (Coach, DRI) + FAQ: ticket ownership concerns                                        | Generalize references to OneNote / ADO → "shared doc space" / "issue tracker".                                            |
| 5   | `workflow-overview.md`           | Workflow & Board Anatomy                | Visual & narrative overview of board: columns, rails, lifecycle.                   | Practitioners                 | How does work flow? What are the stages?                   | `fundamentals.md` → Task Board (Columns, Rails)                                                                | Replace ADO-specific words with neutral ("work tracker / board"). Keep example rails; mark optional.                      |
| 6   | `wip-and-flow.md`                | WIP, Flow & Limits                      | Rationale + policies for limiting work & preventing bottlenecks.                   | Practitioners, coaches        | Why limit WIP? What rules apply?                           | `fundamentals.md` → WIP Limits + related bullets in Tickets                                                    | Add small diagram; externalize formula nouns.                                                                             |
| 7   | `tickets.md`                     | Tickets & Sizing                        | Ticket definition, fields, sizing rules, spike tickets, color/tag strategy.        | Practitioners                 | What belongs in a ticket? How small? How to do spikes?     | `fundamentals.md` → Tickets & Spike Tickets + FAQ scaling answers                                              | Neutralize field names (e.g., "Shepherd" keep but define).                                                                |
| 8   | `design-docs.md`                 | Design Docs: Lightweight Shared Context | Purpose, template, signoff process, benefits.                                      | Engineers & reviewers         | Why write them? What’s the minimal good doc?               | `fundamentals.md` → Design Documents + reasons: PR iteration + bugs sections                                   | Provide public-friendly template; remove OneNote brand, replace with "shared doc".                                        |
| 9   | `meetings-and-ceremonies.md`     | Meetings & Cadence                      | Standup, Retrospective, Planning, Starfish Retro, Value Stream Mapping.            | Team facilitators             | What meetings exist? How to run them well?                 | `fundamentals.md` → Meetings, Planning, Starfish, Value Stream Mapping                                         | Clarify timeboxes; add async adaptation tips.                                                                             |
| 10  | `adoption-guide.md`              | Adopting Golazo (90‑Day Trial)          | Stepwise rollout, success criteria, anti-patterns.                                 | Managers, coaches             | How do we transition? How long to trial?                   | FAQ → Transition Q; `fundamentals.md` quick version; reasons (ramp, PR, bug pain)                              | Replace internal expert emails with generic "Community" pointer.                                                          |
| 11  | `communication.md`               | Communication Patterns                  | Channels, review signaling, async norms, social cohesion.                          | All                           | How do we talk? How are reviews surfaced?                  | FAQ → Communication section + `fundamentals.md` → Asynchronous Communication + Teams channels                  | Generalize Teams → "team chat (e.g., Slack / Teams)"; remove mailto.                                                      |
| 12  | `planning-and-prioritization.md` | Planning & WSJF Prioritization          | Lightweight backlog grooming & WSJF method.                                        | Coaches & product leads       | How do we rank work? How often plan?                       | `fundamentals.md` → Planning + quick backlog grooming notes                                                    | Add worked WSJF example; include caution on over-gamification.                                                            |
| 13  | `measuring-success.md`           | Measuring Success & Health Metrics      | Qual + quant metrics, dashboards, signs of drift, anti-patterns.                   | Leads, stakeholders           | Are we improving? What to watch?                           | FAQ → "How do we know if it's working?" + `fundamentals.md` dashboard bullets + reasons (symptom improvements) | Replace ADO references with generic analytics; add leading/lagging metrics table.                                         |
| 14  | `faq.md`                         | Frequently Asked Questions              | Curated answers not covered elsewhere; links back to pages.                        | Broad                         | Edge cases, special situations.                            | Original `faq.md` minus migrated answers; cross-link out.                                                      | De-duplicate; group by theme; remove internal team names.                                                                 |
| 15  | `glossary.md`                    | Glossary                                | Canonical definitions of terms (Shepherd, Rail, Spike, WSJF…).                     | Newcomers                     | What does this term mean?                                  | Terms aggregated from all old docs                                                                             | Alphabetize; each term 1–3 sentences.                                                                                     |
| 16  | `templates.md`                   | Templates & Examples                    | Design doc skeleton, ticket checklist, retro prompts, channel emojis.              | Practitioners                 | Can I copy/paste a starting point?                         | `fundamentals.md` design doc fields; FAQ review emojis; retro sections                                         | Provide copyable markdown; neutralize emoji guidance (optional).                                                          |
| 17  | `origin-and-evolution.md`        | Origin & Evolution                      | High-level history (generic) & rationale lineage (Lean, Kanban, Agile).            | Curious readers               | Where did this come from? Influences?                      | FAQ → origin (sanitize) + fundamentals principles                                                              | Remove specific internal org names & emails; attribute concepts to public methodologies.                                  |
| 18  | `contribution.md`                | Contributing to the Docs                | How to suggest improvements, style guide, IA rationale.                            | External contributors         | How to contribute? Style constraints?                      | New (synthesized) pulling from this IA document                                                                | Reference style choices below.                                                                                            |
| 19  | `style-guide.md`                 | Documentation Style Guide               | Tone, voice, tense, inclusive language, examples.                                  | Maintainers                   | How to keep consistency?                                   | New (derivative) referencing original tone notes                                                               | Codify conversational yet concise tone; public-safe scrub checklist.                                                      |

---

## Migration Mapping (Detailed)

Below each new page is a bullet list of the specific old sections to pull, with transformation
notes.

### 1. `index.md`

- Pull: `old/index.md` intro paragraphs; "Where To Start" bullets (reframed as Callouts).
- Pull: `fundamentals.md` quick version (condense to ~120 words, link deeper pages).
- Pull: `reasons.md` opening rationale (1–2 sentences as teaser linking to Why page).
- Add: Visual map of docs (simple list) + CTA: "Start with Quick Overview video" (retain public
  video links if still valid externally).

### 2. `why-golazo.md`

- Pull: Every heading in `reasons.md` (normalize to sentence case, remove ellipsis prefix).
- Integrate: FAQ answer "How do we know if it's working?" as final validation section.
- Add: Summary table mapping Problem → Golazo Mechanism → Expected Outcome.

### 3. `principles.md`

- Pull: Principles list from `fundamentals.md` (retain bold labels; trim explanations <60 words
  each).
- Add: Short intro linking to Lean/Kanban references (external public URLs).

### 4. `roles.md`

- Pull: Coach & DRI sections from `fundamentals.md`.
- Pull: Relevant FAQ: ticket expertise / ownership & career growth notes ("What happens if someone
  takes a ticket…", "Career progression" excerpt) move to an "Growth & Equity" subsection.
- Add: Optional roles (Metrics Steward, Documentation Steward) synthesized from responsibilities
  described elsewhere.

### 5. `workflow-overview.md`

- Pull: Task Board overview, Columns descriptions (verbatim style with light neutralization), Rails
  intro.
- Cross-link to WIP, Tickets, Planning pages instead of repeating.
- Keep image placeholder (replace internal path `images\board.png` with new
  `/images/board-example.png`).

### 6. `wip-and-flow.md`

- Pull: Entire WIP Limits rationale + enumerated policies.
- Add: Flow efficiency concept (little's law reference) — new, concise.
- Reference: Rails-specific limits (interrupt rail single active) from `fundamentals.md`.

### 7. `tickets.md`

- Pull: Tickets section + Spike Tickets.
- Pull: Fields (Shepherd, Cost Estimate, Dates, Color/Tags) — unify as "Core Fields".
- Add: Sizing checklist (<= 2 week SLA, business value, testable) synthesized from fundamentals.

### 8. `design-docs.md`

- Pull: Design Documents section including template bullets.
- Pull: Reasons page sections on PR iteration & bug backlog as benefit evidence quotes.
- Add: Example minimal design doc (template page cross-linked to `templates.md`).

### 9. `meetings-and-ceremonies.md`

- Pull: Standup, Retrospective, Dashboard, Celebrate & Change, Value Stream Mapping, Planning,
  Starfish Retrospective.
- Add: Meeting anti-patterns list (constructed from causes of delay + FAQ misuses).

### 10. `adoption-guide.md`

- Pull: FAQ: Transition, Downside (curate), Team size.
- Pull: Fundamentals quick version (as Step 0 orientation) REF not duplicated text.
- Add: 90-Day rollout plan (Phase 1 Learn, Phase 2 Full Trial, Phase 3 Optimize) + Success Criteria
  referencing metrics page.

### 11. `communication.md`

- Pull: FAQ: Communication management + Teams channels enumeration.
- Pull: `fundamentals.md` Asynchronous Communication + Dev General / Review / Release / Social
  channel subsections.
- Sanitize: Replace "Teams" with "team chat" and internal email examples with placeholders.

### 12. `planning-and-prioritization.md`

- Pull: Planning section + WSJF formula & explanation.
- Add: Sample backlog snippet + facilitation tips (Planning Poker neutrality, avoid anchoring).
- Cross-link to Tickets (estimation), Measuring Success (throughput), Adoption Guide.

### 13. `measuring-success.md`

- Pull: FAQ "How do we know if it's working?" + fundamentals Dashboard bullet list.
- Add: Leading metrics (Cycle Time, WIP Age, Review Latency) / Lagging metrics (Incident Rate,
  Employee Engagement) definitions.
- Add: Qualitative pulse survey template (3 questions monthly).

### 14. `faq.md`

- Start with existing FAQ but remove questions whose answers are now full pages (Communication,
  Transition, Team Size, Origin, Downsides).
- Add cross-links at top by category.

### 15. `glossary.md`

- Aggregate terms: Coach, DRI, Ticket, Shepherd, Rail, Column, WIP, Spike, WSJF, Value Stream
  Mapping, Starfish Retro, Cycle Time, SLA, Swarm, Interrupt, Planned.
- Provide concise definitions; link each to deeper page.

### 16. `templates.md`

- Pull: Design doc template list (convert bullets into structured markdown form section headings +
  placeholder text).
- Add: Ticket sizing checklist; Retro action item format; Review emoji legend (generic) + accessible
  text alternative.

### 17. `origin-and-evolution.md`

- Pull: FAQ origin section but redact internal team names & emails (replace with generic: "initially
  piloted within large-scale cloud service teams").
- Add: Timeline bullets (Inception → Board evolution → Remote adoption → Public documentation) — new
  narrative.

### 18. `contribution.md`

- New: How to file an issue, style expectations, PR checklist; IA rationale summary referencing this
  doc.

### 19. `style-guide.md`

- New: Tone (conversational, concise, inclusive), Voice (2nd person, active), Tense (present),
  Formatting (one concept per heading, links not raw URLs), Glossary enforcement.

---

## Sanitization & Public Readiness Checklist

For every reused paragraph:

- Remove internal product/team names & distribution lists.
- Generalize product-specific tools (Azure Dev Ops → "work tracker"; OneNote → "shared notes").
- Replace company-only links with public analogues or remove.
- Ensure no confidential metrics or SLAs tied to internal policy (retain generic SLAs like "< 2
  weeks").
- Spell out first use of acronyms (DRI, WSJF, SLA, WIP).
- Confirm images contain no proprietary dashboards or data (use anonymized mockups).

---

## Cross-Page Navigation Model

- Each page opens with 1–2 sentence summary + "Related" inline links.
- Core learning path (numbered breadcrumbs at top of each page): 1) Index → 2) Why → 3) Principles
  → 4) Workflow Overview → 5) Tickets → 6) Design Docs → 7) Meetings → 8) Planning → 9) Measuring
  Success → (Branch to Adoption / Communication / Glossary).
- Glossary terms auto-linked (future enhancement: script for term linting — out of scope here but
  noted).

---

## Preservation Audit (Completeness Matrix)

| Old Section                           | Destination Page(s)            | Notes                        |
| ------------------------------------- | ------------------------------ | ---------------------------- |
| `old/index.md` intro + Where To Start | index.md                       | Condensed and linked         |
| `fundamentals.md` Quick Version       | index.md, adoption-guide.md    | Reused summary               |
| Principles                            | principles.md                  | Direct transfer              |
| Roles (Coach, DRI)                    | roles.md                       | Minor neutralization         |
| Task Board (Columns)                  | workflow-overview.md           | Column list intact           |
| Rails                                 | workflow-overview.md           | With optional rails note     |
| WIP Limits rationale                  | wip-and-flow.md                | Expanded with flow theory    |
| Tickets + Spike Tickets               | tickets.md                     | Unified                      |
| Design Documents section              | design-docs.md + templates.md  | Template split               |
| Meetings (Standup, Retro, Planning)   | meetings-and-ceremonies.md     | Starfish & VSM included      |
| Dashboard stats                       | measuring-success.md           | Enhanced                     |
| Celebrate & Change                    | meetings-and-ceremonies.md     | Subsection                   |
| Value Stream Mapping                  | meetings-and-ceremonies.md     | Subsection                   |
| Planning (WSJF)                       | planning-and-prioritization.md | Formula preserved            |
| Starfish Retro                        | meetings-and-ceremonies.md     | Diagram replaced placeholder |
| Asynchronous Communication + Channels | communication.md               | Genericized                  |
| Reasons intro + all pain points       | why-golazo.md                  | Renamed headings             |
| FAQ full                              | faq.md (+ distributed)         | De-duplicated                |
| Career progression, ticket expertise  | roles.md / faq.md              | Incorporated                 |
| Downsides                             | adoption-guide.md + faq.md     | Balanced perspective         |
| Origin                                | origin-and-evolution.md        | Sanitized                    |

All original conceptual content accounted for; no sections orphaned.

---

## Style & Tone (Excerpt for `style-guide.md`)

- Voice: Direct, second person for guidance ("You can", "Your team"), third person for principles.
- Sentence length: Prefer < 24 words; break long explanatory sentences.
- Avoid: Internal acronyms without expansion; comparative superlatives without evidence (replace
  "best" with concrete outcome claims).
- Inclusive Language: Avoid gendered terms; use "they" singular.
- Accessibility: Provide text alternatives for emoji (e.g., ":eyes:" for 👀) and images; avoid color
  as sole meaning (ticket colors described with label names).

---

## Incremental Migration Plan

1. Create new file scaffolds (empty headings + TODO markers) in `docs/` (phase 1 PR).
2. Migrate content page by page (principles → workflow → tickets) validating link integrity after
   each PR.
3. Add glossary terms as they appear (avoid dead definitions at end).
