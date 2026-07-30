# Hyfin — ready-made pptxgenjs / docx-js snippets

Load this when actually generating a `.pptx` or `.docx` (i.e. the `pptx`/`docx` skills are also in play). These are working starting points for Hyfin's most common layouts — adapt the content, keep the structure and exact hex/fonts. All hex values are bare six-digit strings per pptxgenjs's own requirement (no `#`, no alpha).

## pptxgenjs — cover/title slide

Ink background, reversed wordmark, strapline with the Signal-teal accent bar — the pattern used on every Hyfin cover and section divider.

```js
const pptxgen = require("pptxgenjs");
const pres = new pptxgen();
pres.layout = "LAYOUT_WIDE"; // 13.3in x 7.5in, 16:9 — do this before adding slides

const slide = pres.addSlide();
slide.background = { color: "0B2A33" }; // Ink

slide.addImage({
  path: "assets/hyfin-wordmark-white.png",
  x: 0.6, y: 0.6, w: 2.4, h: 0.83, // matches the asset's 1406:484 aspect ratio — never stretch off-ratio
});

slide.addText("Financing the switch.", {
  x: 0.6, y: 4.6, w: 10, h: 1,
  fontFace: "Outfit", fontSize: 40, bold: true, color: "FFFFFF",
  charSpacing: -0.4, // approximates the -0.02em tight tracking
  margin: 0,
});

// the Signal-teal accent bar — this IS the brand motif, keep it despite pptx's generic "no accent stripes" guidance
slide.addShape(pres.ShapeType.rect, { x: 0.6, y: 5.5, w: 0.5, h: 0.05, fill: { color: "14CDB8" } });

slide.addText("From bills to ownership.", {
  x: 0.6, y: 5.7, w: 10, h: 0.6,
  fontFace: "Outfit", fontSize: 20, color: "BFE6E1", margin: 0,
});
```

## pptxgenjs — KPI / stat row

Mono label, big mono value, one figure in Teal, 1px rules between cells — no boxes, no rounded corners.

```js
const slide2 = pres.addSlide();
slide2.background = { color: "F4F6F6" }; // Canvas

const stats = [
  { label: "MONTHLY VOLUME", value: "$5,900", unit: "B", color: "0B2A33" },
  { label: "GROWTH", value: "4.7", unit: "×", color: "0E8C82" }, // Teal — the one emphasized figure
  { label: "DEFAULT RATE", value: "3.0", unit: "%", color: "0B2A33" },
];
stats.forEach((s, i) => {
  const x = 0.6 + i * 3.2;
  slide2.addText(s.label, { x, y: 0.8, w: 3, fontFace: "Martian Mono", fontSize: 12, color: "5A6868", charSpacing: 0.6, margin: 0 });
  slide2.addText([{ text: s.value, options: { color: s.color } }, { text: s.unit, options: { color: "0A5E56", fontSize: 22 } }], {
    x, y: 1.1, w: 3, fontFace: "Martian Mono", fontSize: 40, bold: false, margin: 0,
  });
  if (i > 0) slide2.addShape(pres.ShapeType.line, { x: x - 0.3, y: 0.8, w: 0, h: 1.1, line: { color: "D7DDDD", width: 1 } });
});
```

## pptxgenjs — footer (every content slide)

```js
function addHyfinFooter(slide, pres, pageLabel) {
  slide.addShape(pres.ShapeType.line, { x: 0.6, y: 7.1, w: 12.1, h: 0, line: { color: "0B2A33", width: 1.5 } });
  slide.addText("HYFIN · BRAND SYSTEM", { x: 0.6, y: 7.15, w: 6, fontFace: "Martian Mono", fontSize: 10, color: "5A6868", margin: 0 });
  slide.addText(pageLabel, { x: 11.3, y: 7.15, w: 1.4, align: "right", fontFace: "Martian Mono", fontSize: 10, color: "5A6868", margin: 0 });
}
```

## docx-js — one-page memo header

Wordmark top-left, mono metadata top-right, 2px Ink rule, TO/FROM/RE block — the letterhead pattern for partner memos and term sheets.

```js
const { Document, Paragraph, TextRun, ImageRun, Table, TableRow, TableCell, WidthType, BorderStyle, HeadingLevel } = require("docx");

const header = new Table({
  columnWidths: [6000, 3660],
  width: { size: 9660, type: WidthType.DXA },
  rows: [new TableRow({ children: [
    new TableCell({
      width: { size: 6000, type: WidthType.DXA },
      children: [new Paragraph({ children: [new ImageRun({ type: "png", data: wordmarkInkBuffer, transformation: { width: 130, height: 45 } })] })],
    }),
    new TableCell({
      width: { size: 3660, type: WidthType.DXA },
      children: [
        new Paragraph({ alignment: "right", children: [new TextRun({ text: "MEMO · CONFIDENTIAL", font: "Martian Mono", size: 16, color: "5A6868" })] }),
        new Paragraph({ alignment: "right", children: [new TextRun({ text: "30 July 2026", font: "Martian Mono", size: 16, color: "5A6868" })] }),
      ],
    }),
  ] })],
});

const rule = new Paragraph({ border: { bottom: { style: BorderStyle.SINGLE, size: 16, color: "0B2A33" } } }); // size 16 = 2pt

const title = new Paragraph({
  heading: HeadingLevel.HEADING_1,
  children: [new TextRun({ text: "Recommendation summary", font: "Outfit", bold: true, size: 32, color: "0B2A33" })],
});
```

## Notes that apply to all of the above

- Never stretch the wordmark off its native 1406:484 aspect ratio — always set width and height together, proportionally.
- Keep every rule/border straight (`ShapeType.line` or a paragraph border), never a rounded shape.
- If a chart is needed, use the host library's native chart object (`addChart` in pptxgenjs) with `chartColors` set from this palette — Ink axis, one Teal series, Signal only on the single point that matters — never a static image of a chart.
