---
paths:
  - '**/*.stories.tsx'
  - '**/*.stories.ts'
---
# Storybook Style Guide

**Scope:** General rules for all Storybook stories. For framework-specific rules, see `react-stories.styleguide.md` or `vue-stories.styleguide.md`.

## Meta Configuration

- **Required:** `component`, `title`, and `parameters.docs.description.component`.
- **Do not set:** `args` or `argTypes` on meta (Controls infers them).
- **Compound components:** Declare `subcomponents` on meta (map each exported part like `Trigger`, `Content`, etc.).
- **Title format:** `<Prefix>/<Category>/<Name>`
  - `Components/...` for UI components (e.g., `Components/Actions/Button`).
  - `Forms/...` for form components.
  - `Blocks/...` for block packages.
  - `Recipes/...` for recipe stories.
  - `Charts/...` for chart components.
- **Component description:** 1-2 plain sentences in `parameters.docs.description.component`. No prop names or API jargon.

## Tags

- Use `tags` only for status (`experimental`, `deprecated`).
- Do not use `tags` for taxonomy, aliases, or package scope.
- **Autodocs:** Enabled globally in the runner's `preview`. Do not set `tags: ["autodocs"]` per file.

## File Layout

1. **Imports:** `preview`, component(s), icons/helpers.
2. **Meta:** Single `preview.meta({ ... })` block.
3. **Fixtures:** Shared sample data (`const`). Must be declared before stories if used in `args`, otherwise at the bottom.
4. **Stories:** Exported in order.

## Story Order

Skip unused groups.

1. **Default:** Minimal, standard use (one instance only).
2. **Visual variants:** `Sizes`, `Shapes`, `Variants` (one axis per story, grid layout).
3. **Functional states:** `Disabled`, `Loading`, `Invalid`.
4. **Composition:** `WithIcon`, `Nested`, `Group`.
5. **Context:** `Controlled`, `Placements`.
6. **Compound:** (For compound+shorthand APIs only) Last story demonstrating `Foo.Root` + subparts.

## Story Implementation

- **Default Story:** Pass props via `args`. Omit default props. No galleries.
- **Other Stories:** One story = one idea. Prefer `args` for single instances, `render` for layout/composition.
- **Layout:** Use `gap-2` in flex wrappers for side-by-side demos. Do not add artificial width constraints (`max-w-*`, `w-*`) on the component under test.
- **Fixtures:** Inline data if used once. Extract to a shared `const` only if used ≥2 times.
- **No single-use helpers:** Do not extract one-off render wrappers or dummy components. Put JSX directly in `render`.

## Sample Data

- **Dummy data only:** No real people or personal handles.
- **Emails/URLs:** `@example.com`, `https://example.com/...`
- **Images:** `https://placehold.co/{w}x{h}` (e.g., `https://placehold.co/600x400` or `https://placehold.co/400` for square). Can add text with `?text=Hello+World`.

## Overlays (Dialog, Popover, etc.)

- `Default` must include an interactive trigger (e.g., `Trigger asChild` + `Button`).
- Add stories for close behavior or sides only if `Default` doesn't cover them.
- Use `useState` / controlled `open` only when demonstrating controlled usage.
