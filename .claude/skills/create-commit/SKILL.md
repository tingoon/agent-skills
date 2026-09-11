---
name: create-commit
description: >-
  Group changed files and create Conventional Commits (one commit per group).
  Use when the user asks to commit, create commits, or invokes create-commit.
---
# Create commit

Group changed files and commit each group with a [Conventional Commits](https://www.conventionalcommits.org/) message, unless the host repo documents a different convention.

The user asked to commit — creating commits is in scope. Do not assume Lefthook or other tooling from this skills pack is installed in the host repo. Do not inspect commitlint configs; suggest tooling in chat only if useful.

Related policy: `git` skill (hooks, footers). Prefer this skill for the commit workflow itself.

## Path scope (optional)

When a path is given (e.g. `create-commit path/to/area`), limit status and diffs to that path:

```bash
git status -- <path>
git diff -- <path>
```

## Steps

1. **Gather context** (parallel):

   ```bash
   git status
   git diff
   git log -5 --oneline
   ```

2. **Pre-check** — run the project’s usual verify commands when they exist (lint, type-check, tests). If checks fail, fix before grouping. If none are defined, skip and note that in the summary.

3. **Group** by feature, change type, or dependency order (e.g. refactor before feat; schema before generated code). Prefer smaller commits. Do not mix unrelated concerns in one commit.

4. **Commit each group**
   - Stage: `git add <paths>`
   - Message: `<type>(<scope>): <description>`
     - **type:** `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `ci`, `perf`, …
     - **scope:** optional; area of the change (omit when cross-cutting)
     - No `Co-authored-by:` / `Signed-off-by:` footers unless the user asks
   - If a hook auto-fixes files, create a **new** commit — do not amend unless the user explicitly asks and amend is safe

   ```bash
   git commit -m "$(cat <<'EOF'
   type(scope): description

   EOF
   )"
   ```

## Verification

- [ ] Pre-check passed or skipped with reason
- [ ] Every in-scope file in exactly one group
- [ ] Dependencies ordered correctly within the series
- [ ] No mixed types per commit; no secrets staged
- [ ] `git status` clean for the intended scope (or only intentional leftovers)
