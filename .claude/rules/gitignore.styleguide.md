---
paths:
  - '**/.gitignore'
---
# Gitignore

- Same pattern across packages/apps → root `.gitignore` once; folder-local only → that directory’s `.gitignore`
- Tool-owned generated trees → that tool’s nested `.gitignore`; do not duplicate in root
- Within a group: directories with trailing `/`, then file globs, then `!` negations last
- Comment by lifecycle (deps, build, secrets, logs, caches, OS); one lifecycle per section
- Prefer default-deny + `!` over listing every volatile generated path
- Ignore regenerable trees where they live — do not blanket-ignore committed importable codegen (e.g. `*.gen.*`) then negate exceptions
