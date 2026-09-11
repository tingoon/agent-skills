# Agent Skills

This repo is a **skills and rules** library for any project. Skills use the [Agent Skills](https://agentskills.io/home) format; rules follow [Cursor Rules](https://cursor.com/docs/rules). [rulesync](https://rulesync.dyoshikawa.com/) generates Cursor / Claude Code trees.

Edit [`skills/`](./skills/) and [`rules/`](./rules/). Never edit generated `.cursor/skills/`, `.claude/skills/`, or `.cursor/rules/` directly. After changes: `bun run sync`.

## References

| Kind | Author under | Spec / docs |
| ---- | ------------ | ----------- |
| Skills | `skills/` | [Agent Skills - Specification](https://agentskills.io/specification), [Agent Skills - Best Practices](https://agentskills.io/skill-creation/best-practices) |
| Rules | `rules/` | [Cursor Rules](https://cursor.com/docs/rules) |

## Setup

```bash
bun install
bun run sync
```

## Agent notes

1. User chat instructions win.
2. If a skill here matches the task, follow it.
3. Do not invent parallel workflows; extend or add under `skills/` or `rules/`.
4. When authoring or changing **skills**, follow [agentskills.io](https://agentskills.io/home).
5. When authoring or changing **rules**, follow [cursor.com/docs/rules](https://cursor.com/docs/rules).

Details: [README.md](./README.md), [CONTRIBUTING.md](./CONTRIBUTING.md).
