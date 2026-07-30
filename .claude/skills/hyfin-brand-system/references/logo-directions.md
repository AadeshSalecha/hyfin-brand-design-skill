# Hyfin — shortlisted logo directions (exploratory, not final)

The primary wordmark (`assets/hyfin-wordmark-ink.png` / `hyfin-wordmark-white.png`, Direction A) is the current, recommended logo — use it by default. These four directions are shortlisted alternates still under discussion. None of them have production asset files; they exist only as construction notes below. Only bring these up if someone explicitly asks to explore logo variants, a compact mark for a narrow space, or an alternate lockup.

## Direction B — Ink enclosure
The wordmark reversed to white, set inside a solid Ink (`#0B2A33`) block, with a 6px Signal-teal (`#14CDB8`) rule under it. An authoritative, self-contained lockup — good for covers, seals, or partner co-branding where the mark needs its own field.

## Direction D — Stacked monogram
The bridge glyph (see below) inside a 3px Ink-outlined square tile, stacked above the wordmark. A vertical lockup for narrow columns or a social avatar.

## Direction F — Split wordmark
"HY" set in Ink, "FIN" set in Teal, in one continuous word — reads as the two sides of the business (institutional / consumer) in a single mark. Paired with a 2:3 ratio bar (Ink : Teal) underneath.

## Direction H — Bracket enclosure
Teal (`#0E8C82`) brackets, ~5px thick, on either side of the plain wordmark — gives the mark its own field without fully boxing it in, lighter than Direction B.

## The bridge glyph (compact mark)

The reusable icon/favicon device: a horizontal bar (the "bridge," entering at the crossbar height of the H) plus two vertical strokes. As an SVG (100×100 viewBox):

```html
<svg viewBox="0 0 100 100">
  <rect x="8"  y="43" width="46" height="14" fill="CURRENT_OR_ACCENT_COLOR"/>  <!-- bridge bar -->
  <rect x="38" y="20" width="14" height="60" fill="INK_OR_WHITE"/>              <!-- left vertical -->
  <rect x="72" y="20" width="14" height="60" fill="INK_OR_WHITE"/>              <!-- right vertical -->
</svg>
```

Used as a compact mark (app icon/favicon/avatar): Teal fill with a white glyph, or Ink fill with a Signal-teal bridge bar and white verticals, or white/light background with an Ink glyph and 2px `#C2CACA` border. Never rounded — square tile, square glyph.
