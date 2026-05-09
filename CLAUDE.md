# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Not an application — a **Claude Code skill curation workspace**. There is no build, no test suite, no package manifest, and no runtime. The artifacts are SKILL.md bundles (markdown + YAML frontmatter, sometimes with `references/`, `scripts/`, `templates/`, `examples/`) that Claude Code loads as specialized capabilities.

A "task" here almost always means: author a new skill, edit an existing skill's prompt/references, or refresh skills synced from upstream.

## Layout

- [.claude/skills/](.claude/skills/) — the full active skill library (~50 skills) Claude Code loads at startup.
- [.agents/skills/](.agents/skills/) — a subset (13 skills) that mirrors the HyperFrames family. Files here are **identical copies** of their `.claude/skills/` counterparts, kept in sync because some agent contexts read from `.agents/`. Edit one, edit the other.
- [skills-lock.json](skills-lock.json) — pins the 13 HyperFrames skills to specific content hashes from the upstream `heygen-com/hyperframes` GitHub repo. These skills are **vendored, not authored here** — do not hand-edit them; they will be overwritten on the next sync. If a behavior change is needed, propose it upstream.

## Skill categories

Three groups, each with different editing rules:

1. **Vendored / synced (read-only here)** — the 13 skills listed in `skills-lock.json`: `hyperframes`, `hyperframes-cli`, `hyperframes-media`, `hyperframes-registry`, `animejs`, `css-animations`, `gsap`, `lottie`, `three`, `waapi`, `tailwind`, `website-to-hyperframes`, `remotion-to-hyperframes`. Source of truth is `heygen-com/hyperframes`.
2. **Anthropic-published** — e.g. `canvas-design`, `brand-guidelines`, `docx`, `pdf`, `pptx`, `xlsx`, `frontend-design`, `mcp-builder`, `skill-creator`, `web-artifacts-builder`, `webapp-testing`, `algorithmic-art`, `internal-comms`, `doc-coauthoring`, `theme-factory`, `ui-ux-pro-max`, `claude-api`, `slack-gif-creator`. Treat as upstream — only patch with intent.
3. **Locally-authored** — the `mkt-kane-*` family (Vietnamese marketing/content strategy: Brendan Kane communication algorithm, Daniel Wall / Mark Rober / Veritasium / Matt d'Avella / Tanner Leatherstein / Sabrina Ramonov / Dr. Julie Smith formats), and `youtube-trend-finder`. Edit these freely — they are the user's own work.

## Working on skills

Each skill is a directory with `SKILL.md` at the root. The frontmatter `name` and `description` are load-bearing — `description` is what Claude Code matches against user input to decide whether to invoke the skill, so be specific about trigger phrases (the `mkt-kane-*` skills illustrate this with Vietnamese trigger lists like `'viết reels jenga'`, `'viết fb post 5 rules'`).

When creating or improving a skill, use the `skill-creator` skill — it owns the lifecycle (draft → eval → iterate → optimize description). Its scripts live in [.claude/skills/skill-creator/scripts/](.claude/skills/skill-creator/scripts/) (`run_eval.py`, `aggregate_benchmark.py`, `improve_description.py`, etc.) and are invoked by the skill itself, not by the user directly.

## Two gotchas worth flagging

- **Path with spaces.** The repo lives at `/Users/tonyhoang/Documents/claude code 2 days/` — quote it in shell commands.
- **Mirror discipline.** When editing a skill present in both `.claude/skills/` and `.agents/skills/`, change both. They must stay byte-identical, and `.agents/` is downstream of `skills-lock.json` so any change must be reverted on the next sync — fix it upstream instead.
