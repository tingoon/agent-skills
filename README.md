# Agent Skills

Reusable [Agent Skills](https://agentskills.io/home) and [Cursor Rules](https://cursor.com/docs/rules) for any project. Authored under `skills/` and `rules/` and generated for Cursor and Claude Code via [rulesync](https://rulesync.dyoshikawa.com/).

## Skills

| Skill | Use when |
| ----- | -------- |
| `create-commit` | Grouping changes into Conventional Commits |
| `ux-writing` | UI copy, microcopy, tone |

## Rules

| Rule | Globs |
| ---- | ----- |
| `env.styleguide` | `**/.env`, `**/.env.*` |
| `gitignore.styleguide` | `**/.gitignore` |
| `typescript.styleguide` | `**/*.ts`, `**/*.tsx`, `**/*.mts`, `**/*.cts` |
| `react.styleguide` | `**/*.tsx`, `**/*.jsx` |

File-scoped; auto-attached when matching files are in context ([Cursor Rules](https://cursor.com/docs/rules)).

## Setup

```bash
bun install
bun run sync
```

Edit `skills/` and `rules/`. Do not hand-edit generated `.cursor/` or `.claude/` trees.

## Use

In Cursor or Claude Code, invoke by name (`/create-commit`) or describe the task so the agent matches the skill description.

Install into another project with your usual skills/rulesync workflow (for example `npx skills add <owner>/agent-skills` or rulesync declarative sources with no custom `path` — defaults to repo-root `skills/` and `rules/`).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT
