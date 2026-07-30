# Hyfin — color ramps, components & data-viz

Load this when the task involves a table, chart, button, card, KPI block, or when you need a tonal step beyond the five core colors in SKILL.md.

## Full tonal ramps

**Hyfin Teal** (primary brand color)
| Step | Hex |
|---|---|
| 100 | `#DCEDEA` |
| 300 | `#9FD1CA` |
| 500 (base) | `#0E8C82` |
| 700 (use for text) | `#0A5E56` |
| 900 | `#06423D` |

**Deep Ink** (structure)
| Step | Hex |
|---|---|
| 100 | `#E3E8E8` |
| 300 | `#93A2A2` |
| 500 | `#3C555C` |
| 700 | `#15343D` |
| 900 (base) | `#0B2A33` |

**Cool neutrals:** Canvas `#F4F6F6` · Surface `#FFFFFF` · Grey100 `#E9EDED` · Grey200 `#D7DDDD` · Grey300 `#C2CACA` · Grey500 `#7C8A8A` · Grey600 `#5A6868`

**Use light steps (100–300)** for tinted fills/hover states, **500 as the base**, and **dark steps (700–900)** for text on a tinted fill.

## Buttons / CTAs

- Flush-left label, no centering, no rounded corners.
- Primary: solid Ink or solid Teal (`#0E8C82`) fill, white text.
- Secondary: 2px Ink outline, no fill.
- Ember (`#F2A65A`) fill with dark Ink text — reserved for consumer-facing promotional CTAs only (e.g. "Check my offer"), never for institutional/internal actions.

## Tables

- Header row: Ink `#0B2A33` background, white or Teal-100 (`#DCEDEA`) mono text, uppercase, letter-spacing ~0.08em.
- Body rows alternate white / Canvas `#F4F6F6` (zebra striping), separated by 1px `#D7DDDD` rules.
- Numeric columns: right-aligned, Martian Mono, tabular. Negative numbers in parentheses, not a minus sign.
- Totals/highlight row: Teal-100 (`#DCEDEA`) fill, 2px Ink top border, figures in Teal 700 (`#0A5E56`).

## Cards / document mockups

- White surface, 2px Ink border. No radius.
- One Teal callout strip or box for the single headline number/stat — don't add a second colored callout on the same card.
- A soft shadow is acceptable only when mimicking a physical sheet of paper (e.g. a memo or PDF mockup), never on flat UI chrome.

## KPI / stat blocks

- Mono label (Grey600, letter-spacing ~0.06em) + a large Martian Mono value + a small delta in Ink or Teal 700.
- Separate stacked KPI blocks with 1px rules, not boxes/cards.
- A number always carries its unit as a small Teal-700 suffix character (e.g. `$5,900` + a smaller `B`).

## Icons

- Base library: Lucide, restyled — 24px grid, 2px stroke, square caps and joins (no rounded stroke ends), zero corner radius.
- Ink `#0B2A33` by default. Reserve Teal/Signal for the one glyph that's actually active/selected.

## Charts & data-viz

- Ink axis/baseline, 2px stroke, drawn last so bars sit on top of an unbroken line.
- One Teal (`#0E8C82`) data series. Signal (`#14CDB8`) reserved for the single point that matters (a peak bar, an endpoint, the best score) — never used as a whole series.
- Flat fills only, no gradients, no gridlines, no chart junk. Axis/value labels in Martian Mono.
- Approved chart types: line, bar, stacked bar, donut, area, single-stat callout.

## Scoring-matrix legend (when comparing options in a table)

Best = Teal `#0E8C82` · Good = Teal-tint `#6FBDB4` · Partial = Grey300 `#C2CACA` · Limited = Grey100 `#E9EDED`.

## Spreadsheet / financial-model cell-color convention

This is a **separate system from the brand palette** — it's the standard finance modeling convention, used only inside Google Sheets models, never in a brand-facing doc or slide:

- Blue `#1A56DB` = hard-coded input/assumption (the only cells anyone should type into)
- Black `#0B2A33` = formula calculated on this tab
- Green `#0A7F53` = a link pulled from another tab
- Teal fill `#DCEDEA` = the key output/result row

Other modeling conventions: units belong in the row label, not the cell; negatives in parentheses; one assumptions block per tab; tab order Inputs → Model → Outputs.
