# Tingoon Agent Skills

This repo is a **skills and rules** library. Skills use the [Agent Skills](https://agentskills.io/home) format; rules follow [Cursor Rules](https://cursor.com/docs/rules). [rulesync](https://rulesync.dyoshikawa.com/) generates Cursor / Claude Code trees.

Edit [`.rulesync/skills/`](./.rulesync/skills/) and [`.rulesync/rules/`](./.rulesync/rules/). Never edit generated `.cursor/skills/`, `.claude/skills/`, or `.cursor/rules/` directly. After changes: `bun run sync`.

## References

| Kind | Author under | Spec / docs |
| ---- | ------------ | ----------- |
| Skills | `.rulesync/skills/` | [Agent Skills - Specification](https://agentskills.io/specification), [Agent Skills - Best Practices](https://agentskills.io/skill-creation/best-practices) |
| Rules | `.rulesync/rules/` | [Cursor Rules](https://cursor.com/docs/rules) |

## Setup

```bash
bun install
bun run sync
```

## Agent notes

1. User chat instructions win.
2. If a skill here matches the task, follow it.
3. Do not invent parallel workflows; extend or add under `.rulesync/skills/` or `.rulesync/rules/`.
4. When authoring or changing **skills**, follow [agentskills.io](https://agentskills.io/home).
5. When authoring or changing **rules**, follow [cursor.com/docs/rules](https://cursor.com/docs/rules).

Details: [README.md](./README.md), [CONTRIBUTING.md](./CONTRIBUTING.md).
