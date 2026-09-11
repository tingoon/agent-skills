# Tingoon Agent Skills

Reusable [Agent Skills](https://agentskills.io/home) and [Cursor Rules](https://cursor.com/docs/rules) for Tingoon projects. Authored under `.rulesync/` and generated for Cursor and Claude Code via [rulesync](https://rulesync.dyoshikawa.com/).

## Skills

| Skill | Use when |
| ----- | -------- |
| `create-commit` | Grouping changes into Conventional Commits |
| `ux-writing` | UI copy, microcopy, tone |

## Rules

| Rule | Globs |
| ---- | ----- |
| `env` | `**/.env`, `**/.env.*`, `**/shared/env.ts`, `**/shared/env/**` |
| `gitignore` | `**/.gitignore` |
| `typescript` | `**/*.ts`, `**/*.tsx` |
| `react` | `**/*.tsx` |

File-scoped; auto-attached when matching files are in context ([Cursor Rules](https://cursor.com/docs/rules)).

## Setup

```bash
bun install
bun run sync
```

Edit `.rulesync/skills/` and `.rulesync/rules/`. Do not hand-edit generated `.cursor/` or `.claude/` trees.

## Use

In Cursor or Claude Code, invoke by name (`/create-commit`) or describe the task so the agent matches the skill description.

Install into another project with your usual skills/rulesync workflow (for example `npx skills add <owner>/agent-skills` or rulesync declarative sources).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT
