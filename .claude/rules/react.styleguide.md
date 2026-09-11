---
paths:
  - '**/*.tsx'
  - '**/*.jsx'
---
# React

- File names: kebab-case (`sign-in-form.tsx`); named exports only
- One primary component per file; colocate private helpers only when unused elsewhere
- Components: PascalCase; handlers: `onX` (props), `handleX` (local)
- Booleans: `is` / `can` / `should` / `has` (`isOpen`, `canClose`)
- Functional components only; props type `ComponentNameProps` (or `Props`), destructured in params
- Prop order: variant → state → content → events → `className`/`classNames` → rest
- Do not redeclare fields from `extends ComponentProps<…>`; root styling is `className` (not `rootClassName`)
- Body order: refs → context/external hooks → local state → queries/mutations → derived → handlers → effects → subscriptions → early returns → JSX
- Extract non-trivial logic into `useX` hooks; complete `useEffect` deps; memoize only when needed
- Prefer `<>` over wrapper `div`s; list keys: stable ids, not array index
- No `forwardRef` (React 19 `ref` prop); no `defaultProps` — use destructuring defaults
- Leave attribute/key sort to the host formatter; do not hand-sort
