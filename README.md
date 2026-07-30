# Hyfin Brand Design Skill

A Claude Skill that packages Hyfin's brand identity system — exact colors, typography, locked voice/strapline, logo usage, and layout/component rules — so anyone on the team can invoke it while drafting or formatting Hyfin-branded material (Google Docs, Google Slides, memos, one-pagers, emails, product copy).

Source: derived from the Hyfin Brand System deck and design-language spec exported from Claude Design.

## Use it

- **Install to your Claude profile:** download [`hyfin-brand-system.skill`](./hyfin-brand-system.skill) and use Claude's "Save skill" action to add it to your personal skill library, so it's available everywhere you use Claude.
- **Use it in this repo:** clone this repo and open Claude Code inside it — the skill at `.claude/skills/hyfin-brand-system/` is auto-discovered as a project skill and can be invoked with `/hyfin-brand-system`.

## Contents

- `.claude/skills/hyfin-brand-system/SKILL.md` — voice, color, typography, logo, and layout rules, plus how to apply them in Google Docs/Slides.
- `.claude/skills/hyfin-brand-system/assets/` — the two production wordmark files (`-ink` for light backgrounds, `-white` for dark).
- `.claude/skills/hyfin-brand-system/references/` — full color ramps and component specs (`components.md`), and shortlisted/exploratory logo directions (`logo-directions.md`).
- `hyfin-brand-system.skill` — the packaged, installable skill file.
