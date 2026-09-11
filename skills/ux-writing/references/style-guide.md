# Content Style Guide

Standards for all user-facing copy. Adapted from [Atlassian Design — Content](https://atlassian.design/foundations/content) — adopt the writing craft; do not copy Atlassian brand personality.

Workflow: [../SKILL.md](../SKILL.md). Examples: [examples.md](examples.md).

Upstream detail: [Inclusive writing](https://atlassian.design/foundations/content/inclusive-writing) · [Language and grammar](https://atlassian.design/foundations/content/language-and-grammar) · [Voice and tone](https://atlassian.design/foundations/content/voice-tone) · [Date and time](https://atlassian.design/foundations/content/date-time) · [Designing messages](https://atlassian.design/foundations/content/designing-messages)

---

## Voice and tone

**Voice (stable):** clear, practical, respectful, confident without hype.

**Tone (situational):**

| Situation | Tone | Notes |
| --------- | ---- | ----- |
| Errors, warnings, blocked tasks | Direct, calm, actionable | Name the problem; say what to do next. No humor. |
| First-run, new features, confusion | Clear and slightly more instructional | Prefer concrete steps over cleverness. |
| Success, completion | Brief acknowledgment | Light warmth OK; no exclamation spam or jokes. |
| Everyday chrome (labels, buttons, nav) | Neutral and concise | Get out of the way. |
| Promotional or campaign copy | Clear benefit, still plain language | Brand can be warmer; no idioms; no hype stacking. |

**Principles:**

- Tell people only what they need **now**.
- Prefer accurate description over promotional language.
- Delight = small flourish after trust is earned — never in error paths; never every time the same toast fires.
- No idioms, slang, or culture-specific metaphors.

**Dials** (when choosing tone intensity):

| Dial | Intent | Typical surfaces |
| ---- | ------ | ---------------- |
| Inform | Only what is needed now; more prescriptive when confused | Errors, warnings, transient notices |
| Empower | Teach at the decision point; suggest next steps | Dialogs, empty states with CTAs |
| Encourage | Support without patronizing | Info messages, recovery copy |
| Motivate | Show outcomes/benefits when educating | Feature discovery, empty “get started” |
| Satisfy | Practical minimum | Labels, helper text, most chrome |
| Delight | Small flourish after success — rare | Success notices |

Dial **down** warmth when the user may feel fear, anger, confusion, or data-loss risk. Dial **up** clarity for new users and new concepts.

---

## Inclusive language

- **Plain language.** Cut filler (“in order to”, “please note that”). Avoid jargon unless the audience is clearly technical.
- Prefer **they/them** when gender is unknown. Never his/her. Use the pronouns a person specifies when known.
- Prefer **person-first** when you cannot ask preference (“people with disabilities”); use identity-first when a community prefers it and you know that.
- Do not claim an experience is “easy” or “simple”.
- Do not euphemize with patronizing terms (“differently abled”).
- Sensory verbs (`see`, `view`, `watch`) are fine when accurate.
- Prefer `unavailable` / `turned off` over `disabled` in user-facing UI state (code `disabled` attrs stay).
- Descriptive link text — not “Learn more” alone. Visible labels must be accurate (don’t hide meaning only in `aria-label`).
- Forms: ask only what the product needs; prefer open / prefer-not-to-say over forced closed lists; prefer a single **Full name** field unless locale/legal needs require structure.
- Meaningful images: concise **alt text**; decorative: empty alt.

---

## Style and grammar

### Capitalization and headings

- **Sentence case** for titles, headings, menu items, labels, and buttons.
- Capitalize proper nouns and product names.
- Headings: action verb preferred; avoid gerunds (`ing`) in product chrome; no trailing period; prefer statements over questions.
- Buttons / short labels: drop articles (`a`, `an`, `the`) when space matters. Keep articles in longer conversational copy when they help.

### Voice, tense, pronouns

- **Active voice** by default.
- **Present tense** for instructions and live status. Past tense for completed outcomes in titles (“Upload failed”, “File created”).
- Use **you / your / we** when ownership or empathy helps; otherwise omit.
- Prefer **Your** over **My** for user-owned objects (“Your projects”).
- Contractions are welcome when natural (“We can’t load this page”) unless legal/formal tone is required.

### Spelling and abbreviations

- **US English** (Merriam-Webster). `color`, `organization`, `labeled`.
- Spell out product/feature names in customer-facing copy; avoid opaque acronyms on first use.
- Do not use `e.g.`, `i.e.`, `etc.`, or `&` — write “for example”, “that is”, “and”, or list items.
- Plural abbreviations: `1990s`, `PDFs` — no apostrophe.
- Digits for numbers in product copy (`8 characters`), except when a number starts a sentence or “one”/“zero” would be clearer than `1`/`0`.
- Ranges: use **to** (`1 to 4`, `2020 to 2024`), not hyphens, except tight tables/ISO/`FY2008-09`.
- “Step 1 of 2”, not `1/2`.
- Thousands: `4,500` in English source illustrations; format via i18n in code.

### Punctuation

- Oxford (serial) comma.
- Periods on complete sentences in helper text and messages. **No** periods on titles, buttons, menu labels, tooltips (unless multiple sentences).
- Avoid **exclamation marks** in product UI; sparingly in promotional copy only if warranted.
- Prefer two sentences over em-dash asides; don’t use em dashes for ranges.
- Emphasize control names with **bold** in instructions, not quotation marks. Italics sparingly (dynamic values). Never italicize links.
- Prefer “then” over `>` in instructions (screen readers read `>` as “greater than”).
- Hyphenate compound modifiers when needed (`system-wide update`); don’t hyphenate after `-ly` adverbs.

### Lists

- Prefer ≤ 6 items; split longer sets.
- Parallel phrasing. Fragments: lowercase, no trailing periods, lead-in with colon. Full sentences: capitalize + period, no colon lead-in.
- Numbered lists for ordered steps; capitalize + period each step.

### Truncation

Avoid truncation; shorten or wrap. If unavoidable, provide the full string via tooltip and use a real ellipsis (`…`) with no space before it.

---

## Date and time

- **Never hardcode** locale date/time strings. Use i18n / `Intl.DateTimeFormat`.
- Design handoff: specify format length, not a painted English string:

| Length | Date illustration (en-US only) |
| ------ | ------------------------------ |
| full | Sunday, August 14, 2028 |
| long | November 8, 2008 |
| medium | Sep 26, 1952 (space-constrained) |
| short | Prefer ISO `YYYY-MM-DD`; avoid ambiguous `M/D/Y` |

Same idea for time: full / long / medium / short (with or without zone).

- No ordinals (`August 14`, not `August 14th`).
- Relative time (“3 minutes ago”) needs a way to see the absolute timestamp (usually tooltip).
- Prefer “every 2 weeks” over “fortnightly” / “biweekly”; disambiguate “bimonthly”.
- `a.m.` / `p.m.` lowercase with periods and a leading space: `6:30 a.m.` Same-meridiem: `6:30 to 10 p.m.`; cross-meridiem: `10 a.m. to 2 p.m.` Prefer noon / midnight when clearer than 12 a.m. / 12 p.m.

---

## Messages

Choose **message type**, then a **placement pattern** (map to the host UI kit):

| Type | Purpose | Placement pattern |
| ---- | ------- | ----------------- |
| Information | Extra context; not blocking | Inline / section message; optional announcement |
| Success | Action completed | Transient notice or inline success |
| Warning | Risk ahead; possible data loss | Inline / section warning; transient if time-sensitive |
| Error | Something failed; say next step | Inline / section error; field error; transient if global |
| Feature discovery | New capability | Coachmark / spotlight; empty “get started”; modal |
| Empty | Nothing to show | Empty view with next action |
| Critical system | Site-wide outage / data loss | Banner — sparingly |
| Confirm / acknowledge | Low-interaction feedback | Transient notice |
| Blocking decision | User must act | Modal / confirm dialog |

**Writing:**

1. **Title:** short outcome or problem (sentence case; past tense OK for completed/failed actions).
2. **Body:** what happened + **what to do next** (one primary action when possible).
3. Errors: blame the system or state, not the person. Offer recovery when you can. No humor.
4. Success: confirm the outcome; skip filler praise.
5. Warnings: state the risk and whether it is reversible.
6. Empty: say why it’s empty and the best next action.
7. Match visual severity to copy severity (error ≠ witty).

---

## Quick checklist

Before shipping user-facing copy:

- [ ] Sentence case; US English; plain language
- [ ] Active voice; present tense (or past for completed outcomes)
- [ ] Inclusive; no idioms; they/them when unknown
- [ ] No `e.g.` / `etc.` / `&` / unnecessary `!`
- [ ] Dates/times via i18n, not hardcoded English
- [ ] Message type matches placement + severity when applicable
- [ ] Error/empty states include a next step when possible

## Out of scope

- Legal / ToS voice (counsel-owned).
- Separate brand systems for long-form campaign creative (still prefer clarity over hype for product-adjacent copy).
- Atlassian-internal vocabulary — do not use.
