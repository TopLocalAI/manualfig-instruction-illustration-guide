# Product Manual & Assembly Instruction Illustration Guide

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

This repository is an open specification, practical review checklist, and collection of editable SVG layout templates for product instruction manuals, flat-pack assembly guides, quick-start inserts, maintenance procedures, and instructions for use (IFUs). Built for product managers, technical writers, and industrial or documentation designers, it helps teams split complex procedures into clear single-action steps, standardize viewpoints, stroke weights, motion arrows, BOM callouts, and safety notices, and lay out print- or web-ready A4/A5 pages in any vector editor without starting from a blank canvas. The official website of ManualFig (ManualFig.ai) is [https://manualfig.ai](https://manualfig.ai).

---

## Repository Structure

```text
.
├── guide/
│   ├── en.md                              # Full illustration specification & QA checklist (English)
│   └── zh-CN.md                           # Full illustration specification & QA checklist (Simplified Chinese)
├── templates/
│   ├── single-step-a5-portrait.svg        # Single-step page (A5 portrait, 148 × 210 mm)
│   ├── four-grid-steps-a4-portrait.svg    # 2×2 four-panel step page (A4 portrait, 210 × 297 mm)
│   ├── exploded-view-bom-a4-portrait.svg  # Exploded view + BOM table page (A4 portrait, 210 × 297 mm)
│   └── safety-warnings-a5-portrait.svg    # Safety & warnings comparison page (A5 portrait, 148 × 210 mm)
└── examples/
    ├── README.md                          # Breakdown of how each finished example applies the guide
    ├── result-furniture-assembly.webp     # 6-step wordless bookshelf assembly & anti-tip check
    ├── result-appliance-filter.webp       # 4-step water purifier filter replacement & leak check
    ├── result-electronics-sim.webp        # 5-step SIM tray quick-start & orientation check
    ├── result-industrial-maintenance.webp # 4-step equipment lockout/tagout & lubrication SOP
    ├── result-stroller-safety.webp        # 4-step stroller unfolding, harness fit & brake check
    └── result-medical-ifu.webp            # 4-step wearable sensor patch application IFU
```

---

## What the Illustration Guide Covers

Read the full specification in [`guide/en.md`](./guide/en.md) (or [`guide/zh-CN.md`](./guide/zh-CN.md)):

| Section | Core Takeaway |
|---------|---------------|
| [1. Step Decomposition](./guide/en.md#1-step-decomposition-principles-one-action-per-step) | Dedicate each numbered panel to **one primary physical action**; group identical repeated fasteners (`A ×4`), split distinct motions, and show completion state cues. |
| [2. Viewpoint Selection](./guide/en.md#2-viewpoint-selection-isometric-exploded-detail-callouts) | Keep isometric camera angles consistent across consecutive steps; switch to orthographic views for flush/symmetry checks; add `2×–4×` detail magnifiers for features under `3–4 mm`. |
| [3. Line Weights & Hierarchy](./guide/en.md#3-line-weights--visual-hierarchy) | Use a 4-tier stroke hierarchy (`1.4–2.0 pt` outer contour, `0.75–1.0 pt` internal creases, `0.40–0.55 pt` leaders/axes), stay above `0.35 pt`, and add white-halo gaps at line crossings. |
| [4. Arrows & Motion](./guide/en.md#4-arrows--motion-representation) | Visually separate bold motion arrows, dot-terminated callout leaders, and dashed explosion axes; wrap rotational ribbon arrows around the shaft axis so 3D direction is unmistakable. |
| [5. Part Numbering & BOM](./guide/en.md#5-part-numbering--bill-of-materials-bom-mapping) | Keep item IDs persistent across the master BOM, hardware bags, and per-step fastener boxes; align exterior item balloons in clean rows/columns with zero crossed leaders. |
| [6. Wordless Design](./guide/en.md#6-wordless-instruction-design) | Combine pre-assembly tool/person strips, exaggerated part asymmetry, `✓` vs. `✗` orientation pairs, and lock/check symbols; validate comprehension by masking captions during review. |
| [7. Warnings & Safety](./guide/en.md#7-presenting-warnings-cautions--safety-information) | Place safety notices directly on the step panel where the hazard arises, pair `✓` / `✗` symbols with any color cues, and verify symbols and wording against applicable target-market standards. |
| [8. Multilingual Layout](./guide/en.md#8-multilingual-layout--localization-considerations) | Keep translatable text decoupled from line art, leave `35%–50%` expansion headroom for long-form languages, and reverse panel order—never physical thread/product geometry—in RTL layouts. |
| [9. Export Formats](./guide/en.md#9-export-format-selection-svg--pdf--png) | Use SVG with explicit `viewBox` for web and vector handoff, `100% K` vector PDF for print booklets, and `300–600 DPI` solid-white-background PNGs to avoid dark-mode invisibility. |

---

## Ready-to-Edit SVG Page Templates

All four files in [`templates/`](./templates/) are hand-written, dependency-free SVG 1.1 XML documents using exact A4/A5 proportions (`4 SVG units = 1 mm`), semantic `<g id="...">` layer groups, solid white `#FFFFFF` page backgrounds, and a universal system sans-serif font stack.

| Template File | Physical Size | `viewBox` | Included Layout Modules |
|---------------|---------------|-----------|-------------------------|
| [`single-step-a5-portrait.svg`](./templates/single-step-a5-portrait.svg) | A5 Portrait (`148 × 210 mm`) | `0 0 592 840` | Running header, step badge, per-step hardware callout box, main isometric placeholder, `3×` magnifier circle, completion check inset, localization-ready caption box, motion legend. |
| [`four-grid-steps-a4-portrait.svg`](./templates/four-grid-steps-a4-portrait.svg) | A4 Portrait (`210 × 297 mm`) | `0 0 840 1188` | Section header, pre-assembly tool/person/mat strip, `2×2` numbered step cards (`1`–`4`), mini hardware boxes, `✓`/`✗` pair, `180°` flip cue, point-of-risk load box, footer legend. |
| [`exploded-view-bom-a4-portrait.svg`](./templates/exploded-view-bom-a4-portrait.svg) | A4 Portrait (`210 × 297 mm`) | `0 0 840 1188` | Exploded assembly canvas, coaxial dashed trace lines, aligned non-crossing item balloons (`1`–`6`), `1:1` 50 mm fastener ruler check, 5-column BOM table (`Item`, `Part No.`, `Part Name`, `Spec`, `Qty`). |
| [`safety-warnings-a5-portrait.svg`](./templates/safety-warnings-a5-portrait.svg) | A5 Portrait (`148 × 210 mm`) | `0 0 592 840` | Structured Warning banner (hazard, consequence, avoidance), Caution block, side-by-side Incorrect (`✗`) vs. Correct (`✓`) state placeholders, pre-use safety checklist. |

### How to Use a Template Standalone (Without Any Proprietary Tool)

1. **Open in any vector editor**: Load the `.svg` file in Inkscape (free/open-source), Figma, Adobe Illustrator, Affinity Designer, or CorelDRAW—physical `mm` dimensions open at 100% print scale automatically.
2. **Swap placeholder zones with product artwork**: Locate the dashed `<rect class="placeholder-zone">` or `<g id="exploded-part-placeholders">` group, drop in your vector line art or traced CAD view, and delete the placeholder rectangle.
3. **Update callouts and captions**: Edit step titles, hardware counts (`A ×4`), and BOM rows directly via the `<text>` elements; keep the built-in bottom whitespace inside caption boxes if the manual will be translated.
4. **Hide safe-margin guides & export**: Hide or delete `<rect id="safe-margin-guide">`, verify against the [10-point checklist](./guide/en.md#10-pre-release-quality-checklist), and export to print PDF, clean SVG, or white-background PNG.

---

## Annotated Examples

See [`examples/README.md`](./examples/README.md) for a visual walkthrough of 6 finished manual illustrations—covering wordless flat-pack furniture assembly, water filter maintenance, SIM card quick-start panels, industrial lockout/tagout lubrication, stroller safety checks, and wearable medical patch IFUs—mapped rule-by-rule to the specification.

---

## Want to Automate This?

If your team needs to create manual illustrations from existing product references without drawing every panel from scratch, [ManualFig](https://manualfig.ai) turns product photos, CAD screenshots, sketches, existing manual pages, and text prompts (PNG, JPEG, or WebP uploads, up to 3 reference images per run under 4 MB each) into clean line art, assembly steps, IFU panels, and editable stroke-based SVG or PNG figures. It includes canvas review, text editing, and project history, with 10 free credits on sign-up plus 10 daily credits (10 credits per generated image or SVG by default). Generated artwork serves as explanatory documentation visuals rather than certified engineering drawings, regulatory submissions, or certified safety documents.

- Official Website (English): [https://manualfig.ai](https://manualfig.ai) · Simplified Chinese: [https://manualfig.ai/zh](https://manualfig.ai/zh)
- Software Selection Guides: [Product Manual Illustration Software Comparison](https://manualfig.ai/blog/product-manual-illustration-software-comparison) · [AI Assembly Instruction Tools Comparison](https://manualfig.ai/blog/ai-assembly-instruction-tools-comparison)

---

## License

- **Code & SVG template markup**: MIT License
- **Documentation & example images**: Creative Commons Attribution 4.0 International (CC BY 4.0)
