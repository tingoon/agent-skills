# Contributing

This repository publishes **Agent Skills** only. Skills follow the [Agent Skills specification](https://agentskills.io/specification).

## Principles

1. **Specific checklists** over vague advice.
2. **Process over prose** — ordered steps and verification.
3. Every `SKILL.md` ends with a **Verification** section.
4. Keep `SKILL.md` lean; put long detail in `references/` (one level deep).
5. **One skill per workflow** — own folder + `SKILL.md`; do not nest invokable workflows as loose markdown.

## Add a skill

1. `mkdir .rulesync/skills/my-skill`
2. Add `SKILL.md` — `name` must match the folder (lowercase, hyphens):

   ```yaml
   ---
   name: my-skill
   description: What it does. Use when [triggers].
   ---
   ```

3. Optional: `references/`, `scripts/`, `assets/`
4. `bun run sync`
5. Commit `.rulesync/skills/` and generated `.cursor/skills/` / `.claude/skills/`

## Test

Open this repo in Cursor or Claude Code and invoke `/my-skill` or a matching prompt.
