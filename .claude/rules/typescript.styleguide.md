---
paths:
  - '**/*.ts'
  - '**/*.tsx'
  - '**/*.mts'
  - '**/*.cts'
---
# TypeScript Style Guide

Baseline: [Google TS Style Guide](https://google.github.io/styleguide/tsguide.html) + [TSDoc](https://tsdoc.org/). Where this file conflicts, this file wins.

## Naming & files

- File names: kebab-case (`query-parser.ts`)
- Types / interfaces: PascalCase; values: camelCase; constants that are true constants: `SCREAMING_SNAKE_CASE` only when immutable and module-scoped
- Prefer named exports; default export only when the host convention requires it

## Types

- Prefer `unknown` over `any`; narrow with type guards / discriminated unions before use
- Prefer `type` for unions, intersections, mapped, and utility compositions; `interface` when the shape may be extended or implemented
- Prefer const objects + union types over `enum`
- Use `satisfies` and const type parameters where they improve inference without widening
- Prefer `readonly` / `Readonly<>` for data that must not mutate
- Avoid non-null assertions (`!`) and `as` casts; narrow or validate instead. If a cast is unavoidable, keep it local and document why
- Use `import type` / `export type` for type-only imports

## APIs & errors

- Annotate return types on exported functions and public methods; let locals infer
- Validate untrusted input at boundaries (parse → typed value); do not trust external shapes
- Throw `Error` subclasses (or project error types) with causes when rethrowing; never throw bare strings

## Control flow & async

- Prefer `async`/`await` over raw promise chains; always handle or propagate rejections
- Exhaustiveness: use `never` checks on discriminated unions so new variants fail at compile time

## TSDoc

- Third person, present tense ("Returns…"); skip when the type is self-explanatory
- No JSDoc-only tags; use TSDoc tags only
