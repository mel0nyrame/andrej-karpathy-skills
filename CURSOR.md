# Using this repo with Cursor

This project includes a **Cursor project rule** so the Karpathy-inspired behavioral guidelines apply automatically when you work here.

## In this repository

1. Open the folder in Cursor.
2. The rule [`.cursor/rules/karpathy-guidelines.mdc`](.cursor/rules/karpathy-guidelines.mdc) is committed with `alwaysApply: true`, so you do not need extra installation steps.
3. In Cursor, you can confirm it under **Settings → Rules** (or the project rules UI), where `karpathy-guidelines` should appear.

## Use the same guidelines in another project

**Cursor (recommended):** Copy `.cursor/rules/karpathy-guidelines.mdc` into that project’s `.cursor/rules/` directory (create the folders if needed). Adjust or merge with existing rules as you like.

**Other tools:** If a stack only supports a root instruction file, copy [`CLAUDE.md`](CLAUDE.md) into that project instead (or merge its contents into your existing instructions).

## Optional: personal Agent Skills

If you want the same content as a reusable skill under `~/.cursor/skills`, use [`skills/karpathy-guidelines/SKILL.md`](skills/karpathy-guidelines/SKILL.md). You can copy or symlink it into your personal skills directory; use whatever layout you use for other skills.

## Claude Code vs Cursor

- **Claude Code:** Install via the plugin marketplace and [`README.md`](README.md) instructions; the plugin exposes the skill from this repo. Per-project use can also rely on `CLAUDE.md`.
- **Cursor:** Use the committed `.cursor/rules/` file as described above. Cursor does not read `.claude-plugin/` or `CLAUDE.md` by default.

## For contributors

The canonical instruction body is **[`skills/karpathy-guidelines/SKILL.md`](skills/karpathy-guidelines/SKILL.md)**. When changing the five principles, copy its body (without YAML frontmatter) to **[`CLAUDE.md`](CLAUDE.md)** and **[`.cursor/rules/karpathy-guidelines.mdc`](.cursor/rules/karpathy-guidelines.mdc)**. All three bodies must match. Keep the Cursor description aligned with the skill description and preserve `alwaysApply: true`.

Keep the English and Chinese README summaries, examples, and plugin descriptions aligned with the same scope. Coding is one application of the general guidelines; the supported explanatory formats are text, diagrams/images, and interactive HTML.

Verify skill frontmatter, both plugin JSON files, relative documentation links, and instruction-body equality after edits. For changes to behavioral rules, also check realistic general and coding tasks: format selection and verification should fit the task, and simple requests should remain simple. These structural checks do not establish that every model will follow the guidelines.
