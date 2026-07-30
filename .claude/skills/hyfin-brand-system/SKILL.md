---
name: hyfin-brand-system
description: Apply Hyfin's brand identity — exact colors, typography, locked voice/strapline, logo usage, and layout/component rules — whenever creating, writing, or formatting anything Hyfin-branded. Use this proactively for any Google Doc, Google Slides deck, memo, one-pager, email, pitch, product copy, or internal document that represents Hyfin, even if the user just says "make a deck," "write a memo," "draft a slide," or "update the doc" without saying "brand" or "on-brand" explicitly — if it's for or about Hyfin and will be seen by someone outside the person's own notes, it should be on-brand. Also use when asked about Hyfin's colors, fonts, logo files, tagline, or messaging.
---

# Hyfin Brand System

Hyfin is financial infrastructure that bridges institutional capital and everyday consumers to make clean energy affordable for billions. The visual system is flat, architectural, and data-forward: ink on a cool ground, one teal accent, strong 2px rules, zero corner radius, everything flush left. When in doubt, remove rather than add.

This skill is the single source of truth for Hyfin's brand — colors, type, voice, and logo are **locked decisions**, not options to improvise around. Apply them exactly (exact hex, not "teal-ish"; the exact strapline, not a paraphrase).

## Voice (locked)

Four fixed lines, each with one job. Never blend them, never edit the strapline's wording or punctuation.

| Rung | Line | Where it's used |
|---|---|---|
| 1. Strapline | **"Financing the switch."** | Locks to the logo: covers, site hero, badges, swag, footers. Never edited, never re-punctuated, never set in mono/all-caps — always sentence case in the display face. |
| 1b. Locked second line | **"From bills to ownership."** | Pairs with the strapline when a two-line lockup is wanted (covers, investor decks). "Ownership" is internal/investor shorthand for CORE — **never say "CORE" to consumers**; consumer-facing, say "power you own." |
| 2. One-liner | **"The financial plumbing for the mass adoption of distributed climate technologies."** | First paragraph of every deck, memo, or intro email. Explains the business; doesn't need to charm. |
| 3. Consumer promise | **"Clean energy, within reach."** | Consumer app/marketing surfaces only. This is the *only* place Ember (`#F2A65A`) and second-person, warmer voice are allowed. |
| 4. Vision & mission | **"Make clean energy affordable for billions in emerging economies."** | Internal north star — hiring, board, about pages. Not marketing copy; don't set it in a hero. |

Mission statement (longer form, for essence/about copy): "Make clean energy technologies affordable for billions of people in emerging economies."

**Voice rules:**
- Two audiences, one voice: institutions read as credible, rigorous, data-forward; consumers read as accessible, human, optimistic. It's two registers of one brand, never two sub-brands or a second logo.
- Personality axes: **Human** (not corporate), **Precise** (not loud), **Optimistic** (not cautious), **Engineered** (not decorative).
- Values to let show through: mission-first, generous collaboration, accountability, humility.
- "Financing" is a verb — it pulls teal forward and lets ink recede to structure. Keep copy active/verb-led where possible.

## Color — use exact hex, always

Ink is for structure and reading; Teal is the brand; Signal is a spotlight, not a fill; Ember is rationed to consumer warmth.

| Role | Hex | Use |
|---|---|---|
| **Deep Ink** | `#0B2A33` | Body text, headings, structure, rules/dividers, dark backgrounds |
| **Hyfin Teal** (primary brand color) | `#0E8C82` | Primary emphasis, links, consumer-side fills, section dividers |
| **Teal 700** | `#0A5E56` | Use this — not Teal 500 — for teal-colored *text* on a light background |
| **Signal** | `#14CDB8` | The single bright accent. One thing per view only: the key figure, an active state, the primary CTA. Never a background field. |
| **Ember** | `#F2A65A` | Positive human warmth, consumer-facing only. Never on institutional data, never a background field. |
| Teal tint (on dark bg) | `#6FBDB4` | Use in place of Teal 700 for eyebrows/labels/footers when the background itself is Ink or Teal — Teal 700 is tuned for a *light* ground and reads too dark on a dark one. |
| Canvas | `#F4F6F6` | Default page/slide background |
| Surface | `#FFFFFF` | Cards, data surfaces |
| Grey 600 | `#5A6868` | Secondary/muted labels, mono captions |
| Grey 300 | `#C2CACA` | Borders, secondary dividers |
| Grey 200 | `#D7DDDD` | Hairline row rules |

Full tonal ramps (100–900 steps) and the separate spreadsheet-modeling color convention (blue/black/green cell-coding — unrelated to the brand palette) are in `references/components.md`.

**Contrast rules:** Ink on Canvas ≈13.5:1, white on Teal ≈4.7:1 — both safe for body text. Never set body text in Signal or Ember on a light ground.

## Typography

- **Display + body:** **Outfit** (400–700). Headings 600–700 weight, tight tracking (`-0.02em`), always flush left, never centered. Body 400, line-height 1.5, keep paragraphs to roughly 72 characters/line for readability.
- **Data + labels:** **Martian Mono** (400–600). Every number, delta, date, footer, page number, and uppercase eyebrow label goes in this face, tabular where possible.
- Both are real Google Fonts (`Outfit`, `Martian Mono`) — in Google Docs/Slides, pick them directly from "More fonts," no need to substitute a system font.

| Token | Size / weight |
|---|---|
| Display | 64–76 / 700 |
| H1 (title) | 40–44 / 700 |
| H2 | 30–32 / 700 |
| H3 | 22 / 700 |
| Body | 17 / 400 (16 in dense documents) |
| Caption | 14 / 500, color `#26424A` |
| Eyebrow | 13–14 Martian Mono, UPPERCASE, letter-spacing 0.16–0.18em, color Teal 700 `#0A5E56` on a light ground, Teal tint `#6FBDB4` on a dark one |

Never set body copy below 12pt in a printable document; micro-type (mono eyebrows, footers, captions) is the one intentional exception.

## Logo

Two real, usable wordmark files are bundled in `assets/`:
- `assets/hyfin-wordmark-ink.png` — the default. Use on white/Canvas/light backgrounds.
- `assets/hyfin-wordmark-white.png` — the reversed mark. Use on Ink (`#0B2A33`) or Teal (`#0E8C82`) backgrounds.

**Never use a grey or "ember-colored" wordmark** — those only exist in the guidelines as *misuse illustrations* (skewed/slanted, recolored), not real assets. If you don't have `-ink` or `-white`, you don't have the logo.

**Rules, no exceptions:**
- Always flush left. Never centered, skewed, italicized, gradient-filled, or re-spaced.
- Always all-caps "HYFIN" — this is fixed lettering in the art itself.
- Clear space around the mark ≈ the height of its leading bridge bar; don't crowd it.
- Minimum size: 24px tall in print, 20px tall on screen. Below that, use the compact bridge-glyph mark instead (see `references/logo-directions.md`) rather than shrinking the wordmark further.
- A stacked/inline lockup with the strapline needs a minimum width of ~120px to stay legible.

For a compact icon/favicon/avatar (not the full wordmark), use the bridge-mark SVGs bundled in `assets/` — see `references/logo-directions.md`. That file also covers a handful of *shortlisted, not-yet-final* alternate wordmark treatments (an ink-enclosure stamp, a stacked monogram tile, a two-tone split wordmark, a bracket enclosure); those are exploratory with no production asset files and should only come up if someone explicitly asks to see logo variants. Default to the plain wordmark.

## Layout

- Ground is Canvas `#F4F6F6`; content sits in a visible grid with equal-width cells divided by 2px Ink rules (major sections) or 1px `#D7DDDD` hairlines (rows).
- Zero corner radius everywhere — no rounded rectangles, no rounded buttons/cards/tables. No drop shadows on flat UI (a soft shadow is fine only to make a document mockup look like paper on a desk).
- Everything flush left: headings, body, button labels (even in a wide button, the label starts at the left padding edge).
- A standard page/slide reads top to bottom as: mono uppercase eyebrow (Teal 700) → H1/H2 title (Outfit bold, tight tracking) → content in a ruled grid → footer (2px Ink rule, "HYFIN · [doc name]" left, page number right, both mono).
- Give sparse content room to breathe (center it vertically) rather than cramming it into a corner — but don't add decoration to fill space.

Component specs (buttons, tables, cards, KPI blocks, charts/data-viz, icon style) are in `references/components.md` — pull that in when the task involves a table, chart, button, or data callout. When actually generating a `.pptx`/`.docx` (the `pptx`/`docx` skills), `references/pptx-docx-snippets.md` has working pptxgenjs/docx-js starting points for the cover slide, KPI row, footer, and memo header.

## Applying this in Google Docs / Slides

There is no tool that formats a live Google Doc/Slide directly. The real pipeline is: build a properly branded `.docx` or `.pptx` (using the `docx` / `pptx` skills — trigger them for the actual file mechanics) and upload it with `Google_Drive__create_file`, which converts it to a native Google Doc/Slides/Sheets file on upload. Only fall back to plain-text/markdown output if there's no Drive access at all.

**This skill's rules override the pptx skill's generic slide-design defaults where they conflict.** The `pptx` skill's own design guidance says *"NEVER use accent lines under titles"* and *"NEVER add decorative color bars or accent stripes"* — good general advice, but exactly backwards for Hyfin: the Signal-teal bar under the strapline and the 2px Ink rules dividing every section **are** Hyfin's visual signature, not AI-generated filler. Keep them. Everything else in the pptx skill's design guidance (one dominant color, strong title/body size contrast, flush-left body text, real charts over decoration) already agrees with this system — Ink dominant, Teal supporting, Signal as the one accent maps directly onto its "one color dominates, one sharp accent" rule.

1. **Fonts** — Outfit for headings/body, Martian Mono for numbers/labels/footers. Both are genuine Google Fonts, so once the file lands in Google Docs/Slides they render exactly right — pptx's "safe font" list (Arial, Calibri, etc.) is about literal Microsoft Office rendering and doesn't apply here. If a deliverable might *also* be opened in real PowerPoint/Word (not just Google's viewer), treat Outfit/Martian Mono as pptx's "QA-unreliable" tier: leave ~10% size slack and don't trust the LibreOffice-rendered QA preview's text-fit for exact overflow.
2. **Colors** — use the exact hex from the table above. In `pptxgenjs`/`docx`-js, hex is bare six digits with no `#` and no alpha (`"0E8C82"`, not `"#0E8C82"` or an 8-digit value) — the extra characters corrupt the file. Reach for Teal 700 `#0A5E56`, not Teal `#0E8C82`, whenever teal is applied to *text* on a light ground.
3. **Logo** — place `assets/hyfin-wordmark-ink.png` on white/light slides or pages, `assets/hyfin-wordmark-white.png` on dark (Ink or Teal) ones, flush left, resized proportionally (never stretched non-uniformly).
4. **Rules & dividers** — a 2pt straight line/border in Ink `#0B2A33` under titles and above footers; square corners on every shape/table (no `ROUNDED_RECTANGLE`).
5. **Footer convention** — small mono text, left "HYFIN · [DOCUMENT OR DECK NAME]", right the page number (e.g. "3 / 12"), both in Grey 600 `#5A6868` or, on a dark background, the teal-tint `#6FBDB4`.
6. **Voice** — open with the one-liner if it's an external-facing doc, use the strapline verbatim wherever a tagline is needed, and never introduce a new tagline or reword the locked lines.

## Do / Don't

**Do:** let the grid show; keep everything flush left; set every figure in Martian Mono; use Signal for exactly one thing per view; divide sections with 2px Ink rules; save Ember for genuine consumer-facing warmth; give layouts air.

**Don't:** round corners or add drop shadows; center headings or body text; set body copy in Teal/Signal/Ember on a light background; skew, recolor, gradient, or re-space the logo; use Signal or Ember as a background fill; introduce fonts outside Outfit/Martian Mono; reword the strapline or one-liner.
