---
name: ux-writing
description: Draft, revise, and review user-facing product copy — labels, buttons, headings, helper text, empty states, alerts, toasts, dialogs, errors, success/warning/info messages, announcements, tooltips, CTAs, alt text, and placeholders — using Atlassian Design Content–adapted standards. Use when writing or editing UI strings, microcopy, UX writing, voice and tone, inclusive language, i18n source English, or when the user asks for a copy review — even if they do not say "content design."
---
# UX Writing

Write and review user-facing strings so they stay clear, inclusive, and consistent. Prefer host product voice/brand docs when they exist; otherwise use this guide.

Upstream craft (not brand voice): [Atlassian Design — Content](https://atlassian.design/foundations/content).

## When to use

- New or revised UI chrome (buttons, labels, nav, form fields, helpers)
- Feedback surfaces (errors, warnings, success, empty states, dialogs, toasts)
- Copy review / rewrite for clarity, inclusive language, or consistent tone
- English source strings for i18n catalogs

**Not this skill:** legal/ToS voice; campaign creative owned by a separate brand system (still prefer clarity over hype when product-adjacent).

## Workflow

```text
UX writing:
- [ ] 1. Context
- [ ] 2. Message type + placement
- [ ] 3. Draft
- [ ] 4. Self-review (gate)
- [ ] 5. Deliver
```

### 1. Context

Ask only what is missing:

- **Surface:** button, label, heading, helper, empty state, inline message, transient notice, dialog, form error, tooltip, long-form, promotional
- **User state:** confident / new / blocked / celebrating / at risk of data loss
- **Locale:** English source defaults; keep strings localizable (no idioms)
- **Constraint:** length limits, truncation, existing title/body/action slots

### 2. Message type + placement

Pick type and placement from [references/style-guide.md — Messages](references/style-guide.md#messages). Map names to the host UI kit. Long-form or promotional: follow voice and grammar; skip placement unless embedding feedback UI.

### 3. Draft

Load [references/style-guide.md](references/style-guide.md) before drafting.

1. Short **title** (outcome or problem; sentence case)
2. **Body** with cause + next step when needed
3. One clear **action** (verb + object; drop articles in tight chrome)

### 4. Self-review (gate)

Do not deliver until the [quick checklist](references/style-guide.md#quick-checklist) passes. Compare against [references/examples.md](references/examples.md).

If a check fails, revise and re-check — same as a validation loop.

### 5. Deliver

1. **Final strings** ready to paste
2. **Message type + placement** (host component names only if known)
3. **Brief rationale** only when meaning or severity changed
4. Optional **alternatives** (max 2) when tone is ambiguous

## Output format

```markdown
### Copy
- **Title:** …
- **Description:** …
- **Action:** …   <!-- if any -->

### Placement
Error · inline/section message (or transient / modal / empty view / …)

### Notes
<!-- only if needed -->
```

For a single label or button, return the string only.

## Example

**Request:** Error when saving fails due to offline network; inline alert with retry.

```markdown
### Copy
- **Title:** We can’t save your changes
- **Description:** Check your connection and try again.
- **Action:** Try again

### Placement
Error · inline/section message
```

## Gotchas

- **Sentence case** everywhere in chrome — not Title Case.
- Blame the **system or state**, not the person, in errors.
- No humor on error/warning/data-loss paths.
- No idioms, slang, or culture-specific metaphors (breaks localization).
- Do not hardcode locale date/time strings — design for i18n / `Intl`.
- Do not claim flows are “easy” or “simple.”
- Prefer descriptive link text over bare “Learn more.”
- Match copy severity to visual severity (error ≠ witty success tone).

## References

| File | Load when |
| ---- | --------- |
| [references/style-guide.md](references/style-guide.md) | Drafting or checking voice, grammar, messages, inclusive language |
| [references/examples.md](references/examples.md) | Self-review — do/don’t pairs and placement examples |
