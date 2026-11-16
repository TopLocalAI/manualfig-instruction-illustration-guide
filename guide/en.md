# Product Manual & Assembly Instruction Illustration Guide

English | [简体中文](./zh-CN.md)

This guide is written for **product managers, technical writers, and industrial or documentation designers** who plan, draw, or review figures for product manuals, quick-start guides (QSGs), flat-pack assembly booklets, maintenance procedures, and instructions for use (IFUs). Every practice documented here is tool-agnostic and grounded in established technical illustration and print production conventions.

> **Compliance Note**: Safety warnings, hazard pictograms, medical device instructions, and juvenile or electrical product disclosures are governed by market-specific regulations. This guide covers general visual communication and layout practices only—always **verify safety symbols, signal words, and mandatory text against the safety symbol and instruction manual standards applicable to your target market**.

---

## Contents

1. [Step Decomposition Principles (One Action per Step)](#1-step-decomposition-principles-one-action-per-step)
2. [Viewpoint Selection (Isometric, Exploded, Detail Callouts)](#2-viewpoint-selection-isometric-exploded-detail-callouts)
3. [Line Weights & Visual Hierarchy](#3-line-weights--visual-hierarchy)
4. [Arrows & Motion Representation](#4-arrows--motion-representation)
5. [Part Numbering & Bill of Materials (BOM) Mapping](#5-part-numbering--bill-of-materials-bom-mapping)
6. [Wordless Instruction Design](#6-wordless-instruction-design)
7. [Presenting Warnings, Cautions & Safety Information](#7-presenting-warnings-cautions--safety-information)
8. [Multilingual Layout & Localization Considerations](#8-multilingual-layout--localization-considerations)
9. [Export Format Selection (SVG / PDF / PNG)](#9-export-format-selection-svg--pdf--png)
10. [Pre-Release Quality Checklist](#10-pre-release-quality-checklist)

---

## 1. Step Decomposition Principles (One Action per Step)

Most assembly and setup mistakes happen not because a drawing lacks artistic polish, but because **too many actions are crammed into a single panel**. When a reader has to locate multiple unfamiliar parts, infer action order, and perform two or more different physical motions inside one frame, skipped washers, reversed panels, and cross-threaded screws follow immediately.

### 1.1 Core Decomposition Rules

- **One primary physical action per numbered panel**: Dedicate each numbered step to a single core motion—such as inserting wooden dowels, seating a shelf onto pins, tightening cam locks, or latching a cover.
- **Merge identical repetitions; split distinct motions**:
  - **Safe to merge**: Inserting four identical dowels (`A ×4`) into four symmetric holes along the same board edge is a single repeated action and belongs in one step.
  - **Must split**: Sliding a cartridge into a housing, twisting a locking collar, and opening a supply valve involve three distinct motion paths and contact points. Split them into separate numbered panels, or pair the main view with numbered sub-panels (`1` → `2`).
- **Separate active parts from completed context**:
  - Draw **only the parts introduced in the current step** at full visual prominence, alongside enough adjacent structure for spatial orientation.
  - Treat components assembled in earlier steps as a unified, calm structural anchor; do not re-label fasteners that are already installed.
- **Show pre-action prerequisites and post-action completion states**:
  - If power must be locked out, a water valve shut off, or a transport clip removed before touching the assembly, make that prerequisite Step 1 or a dedicated pre-action callout—never bury it as an afterthought in body text.
  - Show **what completion looks like** at critical checkpoints: a tray sitting flush with the frame, a latch clicking into place (`CLICK` + closed padlock icon), a status indicator lighting up, or a leak/stability check.

### 1.2 Step Decomposition Decision Table

| Scenario | Avoid | Recommended Practice |
|----------|-------|----------------------|
| Mounting a bracket with two different fastener types | Pointing long screws, short screws, washers, and bracket arrows into one crowded figure | Step 1: Align the bracket and insert locating pins/screws; Step 2: Add washers and tighten locking screws |
| Flipping the product over to work on the back panel | Jumping abruptly to a rear view in the next panel without warning | Add an explicit **whole-object turnover/rotation icon** (e.g., `180°` flip arrow) between steps or at the corner of the step |
| Hidden snap-fit tabs or internal O-ring seating | Showing only the outer cover closing from the outside | Show the cover motion in the main figure and add a magnified detail inset showing the internal tab engagement or seated seal |

---

## 2. Viewpoint Selection (Isometric, Exploded, Detail Callouts)

A good viewpoint lets the reader match the drawing on paper to the physical object in their hands within two seconds. Instruction illustrations prioritize **unobstructed part visibility, unambiguous hole orientation, and spatial continuity across steps** over dramatic perspective.

### 2.1 Axonometric & Isometric Views

- **Default workhorse for assembly and service steps**: Isometric views (120° axis separation, ~30° horizontal tilt) or slightly adjusted trimetric views reveal three faces simultaneously (top, front, side), making 3D insertion paths and hole patterns easy to read.
- **Lock the camera angle across consecutive steps**: Keep the same viewing angle across Steps `1 → 2 → 3` whenever possible. Readers use the unchanged outer silhouette as a mental anchor so newly added parts pop out immediately.
- **Nudge the angle to prevent collinear edge overlap**: Pure mathematical isometric projection sometimes aligns a front vertical edge directly on top of a rear vertical edge. Rotating the azimuth by 5°–10° separates overlapping edges cleanly.

### 2.2 Orthographic (Flat) Views

2D front, side, or top views outperform 3D views in specific cases:
- **Port, button, and indicator maps**: Rear connector panels, control buttons, or SIM card corner notch alignment.
- **Flushness, clearance, and symmetry checks**: Confirming a SIM tray sits flush with the phone rail, checking symmetric five-point harness slack, or marking wall-anchor drilling templates.
- **Posture and tipping comparisons**: Side-profile orthographic drawings make upright anchored furniture vs. forward-tipping unanchored furniture unmistakable at small print sizes.

### 2.3 Exploded Views

- **Pull parts apart strictly along true assembly axes**: Explode components along the exact vector they slide or thread together, connected by thin dashed trace lines (centerlines) from fastener tip to receiving hole.
- **Explode by sub-assembly groups, not "starburst chaos"**: On complex products, separate major modules first (base group, filter cartridge group, cover group) rather than scattering every screw and washer evenly across the page, which forces the entire illustration to shrink.
- **Maintain consistent part scale**: Keep parts at true relative proportions inside the exploded view. When a tiny retaining clip or seal becomes too small to read at scale, enlarge it inside a **detail callout circle** rather than distorting its size in place.

### 2.4 Detail Callout Circles (Magnifiers)

- **When to add one**: Whenever a critical feature measures less than roughly `3–4 mm` at final print size—such as cam-lock arrow slots, filter alignment notches (`Notch` / `Guide`), buckle tongues, or cable polarity keys.
- **Visual rules**:
  - Enclose the zoom view in a clean circle or rounded rectangle at **2×–4×** magnification.
  - Circle the source region on the main figure and connect it with a **single thin leader line, dashed line, or tapered wedge** stopping at the magnifier ring—never run leader lines across the middle of the detail geometry.
  - Include enough surrounding edge context inside the zoom circle so the reader can still tell up from down.

### 2.5 Cutaways & Ghosted Context

- When an action takes place inside a housing (e.g., greasing an internal bearing fitting or engaging a recessed latch), render the outer shell in lighter, thinner strokes or add a localized cutaway edge so the active tool and target part hold maximum contrast.

---

## 3. Line Weights & Visual Hierarchy

Clean technical line art beats raw photography in manuals because **it deliberately filters visual hierarchy**. If every line shares the exact same stroke weight, outer silhouettes, surface seams, leader lines, and background parts flatten into visual noise.

### 3.1 Four-Tier Stroke Weight System (at 100% Print Scale)

Standardize 3–4 stroke weights across a manual, maintaining roughly a **1.8×–2×** step between adjacent tiers:

| Tier | Role | Recommended Weight (pt) | Recommended Weight (mm) | Color Guidance |
|------|------|-------------------------|-------------------------|----------------|
| **L1 Primary Silhouette** | Outer contour of active parts, primary section cuts, hand/tool outlines | `1.4 – 2.0 pt` | `0.50 – 0.70 mm` | Solid black `#111827` / `100% K` |
| **L2 Structural Edges** | Visible internal creases, hole rims, completed background sub-assemblies | `0.75 – 1.0 pt` | `0.26 – 0.35 mm` | Solid black or dark gray `#374151` |
| **L3 Leaders & Fine Detail** | Thread ridges, knurling, callout leader lines, dashed explosion axes | `0.40 – 0.55 pt` | `0.14 – 0.20 mm` | Medium-dark gray `#4B5563` or thin black |
| **L4 Frames & Callout Rings** | Step panel borders, hardware sub-boxes, detail magnifier rings | `0.80 – 1.25 pt` | `0.28 – 0.45 mm` | Neutral gray panels; optional accent on rings |

### 3.2 Minimum Printable Stroke & Crossing Gaps

- **Respect the minimum printable floor**: Avoid hairline strokes thinner than `0.35 pt` (`0.12 mm`) on printed manuals and folded packaging inserts; ultra-thin lines break up on uncoated paper or office laser printers.
- **Use white-halo knockouts (line gaps) at crossings**: Where a callout leader or motion arrow crosses over product geometry, add a `1–1.5 mm` white gap/halo behind the leader so crossing lines never create false corners.
- **Monochrome-first with disciplined single-accent color**:
  - Every figure must remain 100% legible when printed in grayscale or photocopied.
  - When two-color or full-color printing is available, restrict color to **one high-contrast accent hue** (such as deep teal or technical blue) reserved strictly for **step badges, motion arrows, callout rings, and key state indicators**—keep the product line art itself neutral and uncluttered.

---

## 4. Arrows & Motion Representation

Readers rely on arrows to answer "which way do I move this, and how?" Using the same arrow style for static part labels and physical actions causes users to pull or pry on stationary components.

### 4.1 Keep Three Line Roles Visually Distinct

1. **Motion Arrows**: Bold, filled, or wide-shafted directional arrows reserved exclusively for **physical movement or force**.
2. **Callout Leader Lines**: Thin solid lines ending in a **small solid dot** (on a part surface) or connecting cleanly to an item balloon—never styled like motion arrows.
3. **Explosion Axis Lines**: Thin dashed lines (e.g., `3 pt dash / 2 pt gap`) with **no arrowheads**, indicating coaxial alignment between mating parts.

### 4.2 Motion Taxonomy & Drawing Conventions

| Motion Type | Visual Convention | Key Watchout |
|-------------|-------------------|--------------|
| **Linear push / pull / insert** | Straight filled arrow aligned strictly parallel to the axis of travel | Keep a small breathing gap from part edges so the shaft does not merge into the outline |
| **Rotation / twist / screw tightening** | Perspective **curved ribbon arrow** wrapping around the shaft axis (passing visibly in front of and behind the axis) | Flat 2D circular arrows in isometric views look ambiguous; wrapping around the shaft makes clockwise vs. counter-clockwise unmistakable |
| **Hinged lid / pivoting handle** | Curved arc arrow centered on the hinge pivot, optionally paired with a dashed ghost outline of the open position | Match arc curvature to the true swing radius |
| **Compound two-stage action** (e.g., press tab then pull, push in then twist) | Draw two separate motion arrows labeled with small sequence numbers `①` and `②` | Never bend two different motions into a single zig-zag arrow |
| **Peeling film / adhesive liner** | Draw a lifted corner curl paired with a short curving peel arrow | Differentiate the backing liner from the adhesive pad inside a zoom circle using light stippling or hatching |

### 4.3 Sensory Cues & Arrow Legends

- **State & tactile cues**: Pair snap-locks with short burst ticks (`CLICK`) or open-to-closed padlock icons (`🔓 > 🔒`); show flush seating with alignment ticks and a `✓` badge.
- **Page-level arrow legend**: When a procedure combines multiple motion arrows (e.g., `Twist`, `Push up`, `Pull down`), include a compact legend bar along the bottom margin of the page.

---

## 5. Part Numbering & Bill of Materials (BOM) Mapping

Across multi-step assembly manuals and service documentation, item balloons and the Bill of Materials (BOM / parts list) form the master index linking the page, the hardware blister pack, and spare-part ordering.

### 5.1 Numbering Conventions

- **Split structural vs. hardware coding (common in consumer assemblies)**:
  - Structural panels and major sub-assemblies use numerals: `1, 2, 3, ...`
  - Screws, dowels, cam locks, and hex keys from hardware bags use uppercase letters: `A, B, C, ...` (skip `I` and `O` to prevent confusion with `1` and `0`).
- **Unified sequential numerals (common in industrial & service BOMs)**:
  - Number every component in the exploded assembly sequentially (`1, 2, 3, ...`) matching BOM table row numbers directly.
- **Strict document-wide persistence**: Part `B` on the master parts page, on the printed hardware bag, in Step 1, and in Step 5 must always be Part `B`. Never restart part numbering from `1` on each page, and keep **step badges** visually distinct from **item balloons** (e.g., solid filled circles for step numbers vs. outlined white circles or lettered boxes for parts).

### 5.2 Per-Step Hardware Callout Boxes

Place a compact hardware box inside each step panel listing **only the fasteners consumed in that step**:
- Draw recognizable fastener features (Phillips vs. hex socket drive, thread type, washer stacking order).
- State the part code and **per-step quantity** (e.g., `B ×4`), plus critical dimensions (`Ø8×30 mm`) when similar screws of different lengths exist in the kit.
- On the master BOM page, consider including **1:1 actual-size fastener silhouettes** along a printed ruler bar so users can lay physical screws directly on the paper to verify length.

### 5.3 Balloon Placement & BOM Table Columns

- **Aligned, non-crossing leaders**: Arrange item balloons in clean horizontal rows or vertical columns outside the silhouette of the product. Keep leader lines straight or angled consistently, and **never cross two leader lines** or pass a leader through another balloon.
- **Standard BOM table fields**:
  - `Item` (matches the balloon ID in the exploded view)
  - `Part No.` (SKU or spare-part ordering code, optional)
  - `Part Name / Description` (consistent terminology across manual and support site)
  - `Specification` (thread size, length, or material note, optional)
  - `Qty` (total count required per product unit)

---

## 6. Wordless Instruction Design

Products shipped across dozens of countries in a single packaging SKU—such as flat-pack furniture, mounts, and accessories—frequently rely on wordless (or minimal-text) sequences to eliminate repetitive typesetting and multi-booklet printing waste.

### 6.1 Core Building Blocks of Wordless Visual Grammar

1. **Pre-assembly setup strip**: Before Step 1, show required household tools (screwdriver, level, tape measure), recommended person count (1-person vs. 2-person lift), surface protection (assembling on a rug or flattened carton to avoid scratches), and support contact cues.
2. **Exaggerated poka-yoke (asymmetry) cues**: If a board has pre-drilled holes on one face or a finished edge on one side only, make that asymmetry unmistakable in the drawing and add a zoom circle—never draw an asymmetric part as a plain featureless rectangle.
3. **Side-by-side `✓` vs. `✗` panels**: Wherever testing reveals a common orientation or safety mistake, show the correct state (`✓`) next to the incorrect state (`✗`).
4. **Visual completion checkpoints**: Use open/closed padlocks, mating alignment triangles (`▼` / `▲`), spirit-level bubbles, or checkmark badges to communicate pass/fail criteria without prose.

### 6.2 The "Cover-the-Captions" Usability Check

Even on manuals that include written captions, perform a **caption-covered walkthrough** during review: mask every sentence on the page and ask a colleague unfamiliar with the product to explain what part to pick up, which way it faces, and how to confirm it is locked. Wherever they hesitate or guess wrong, fix the illustration (better angle, detail zoom, or `✓`/`✗` pair) rather than writing a longer paragraph to excuse an unclear drawing.

### 6.3 Limits of Wordless Design

Icons alone cannot safely communicate every instruction:
- Non-obvious hazards (chemical incompatibilities, battery thermal risks, medical contraindications, electrical ratings), legal warranties, and regulated disclosures still require clear written text.
- To determine which instructions may rely on pictograms alone and which require translated text in official local languages, **verify against the safety symbol and instruction manual standards applicable to your target market**.

---

## 7. Presenting Warnings, Cautions & Safety Information

Safety visuals exist to prevent injury and product damage at the exact moment a user reaches for a part—not merely to stack legal text at the front of a booklet.

### 7.1 The Proximity Principle

- Front-matter safety summary pages are often required, yet users rarely flip back to page 2 once they are holding a wrench on page 10.
- **Place the safety cue directly inside the step panel that triggers the risk**: show water shut-off right on Step 1 of filter replacement; show power lockout/tagout right on Step 1 before opening an equipment guard; show wall anti-tip anchoring and shelf load limits (`MAX. 25 kg`) right on the final setup panel.

### 7.2 Visual Anatomy of a Warning or Caution Block

An effective safety block combines four elements:
1. **Distinct signal header**: Clear severity tiering (e.g., Danger / Warning / Caution / Notice) set in bold, high-contrast typography.
2. **General hazard, prohibition, or mandatory pictogram**: Clean triangle, prohibition circle-backslash, or mandatory action icon aligned consistently beside the text.
3. **Concise three-part wording**: State **what the hazard is**, **what happens if ignored**, and **how to avoid it** in direct, active sentences.
4. **Pinpoint callout on the product figure**: Mark the exact pinch gap, hot surface, live terminal, untouchable adhesive pad, or center-of-gravity tipping risk on the drawing itself—not an isolated triangle floating in a corner.

### 7.3 Designing `✓` / `✗` Pairs for "Almost Right" Errors

The highest-risk user errors often look nearly right at a casual glance:
- Five-point child harness buckled but left slack (`TOO LOOSE` vs. `SNUG FIT`);
- Folding frame opened without the side latch clicking home;
- Power plug or ribbon cable seated halfway;
- O-ring pinched under a housing lid.

When illustrating `✓` / `✗` pairs:
- **Zoom in on the critical difference** so it remains obvious even when printed on an A5 or A6 booklet page;
- **Never rely on red and green ink alone**: always pair any color cue with bold `✓` and `✗` symbols so monochrome prints and readers with color-vision deficiency can distinguish safe from unsafe states Effortlessly.

### 7.4 Standards & Compliance Verification

- Never invent or approximate certification marks, agency logos, or regulated statutory symbols inside illustrations.
- Symbol geometry, border proportions, signal word definitions, color coding, and mandatory safety wording must always be **verified against the safety symbol and instruction manual standards applicable to your target market**.

---

## 8. Multilingual Layout & Localization Considerations

A manual drafted in English or Chinese often expands into German, French, Spanish, Japanese, Arabic, and more. Planning localization into the illustration architecture saves weeks of manual DTP rework.

### 8.1 Decouple Artwork from Translatable Text

- **Never rasterize body sentences into bitmap artwork**: Keep illustrations clean using numeric or lettered callouts (`1, 2, 3` / `A, B`) and place translatable captions in page-layout text frames or isolated top-level `<text>` groups in SVG.
- Where single-word labels appear inside a detail view (such as `Notch` / `Guide`), keep live editable text layers in the master vector file or replace inline words with callout numbers mapped to a translated legend.

### 8.2 Budget for Text Expansion

- Translating concise English or Chinese copy into German, French, Russian, Spanish, or Portuguese routinely expands character length by **30%–60%** (and short one-word UI/part labels can double in length).
- **Layout headroom rules**:
  - Leave **35%–50% open whitespace** inside step caption boxes, warning banners, and the `Part Name` column of BOM tables in your master template.
  - Prefer full-panel-width caption blocks below figures over cramped narrow sidebars.
  - **Never horizontally condense font width (`< 90%` horizontal scale)** to cram long translations—condensed small type degrades print legibility severely.

### 8.3 Font Stacks, Type Sizes & Reading Direction (LTR / RTL)

- **Universal sans-serif font stacks**: Choose clean sans-serif typefaces with clear numerals (`1` vs. `I`, `0` vs. `O`) and full glyph coverage across Latin and CJK scripts (e.g., `Noto Sans` / system sans-serif stacks).
- **Size and leading guidelines**: Keep printed body text at `8–9 pt` or larger (`7 pt` absolute floor on compact inserts), with `1.3–1.45` line height for Latin scripts and `1.45–1.6` for CJK scripts.
- **Right-to-Left (RTL) localization (Arabic, Hebrew)**:
  - Reverse multi-panel grid reading order from **right to left** (Step `1` at top-right, Step `2` at top-left).
  - **NEVER horizontally mirror-flip the product illustration itself!** Mirroring artwork turns standard right-hand screws into non-existent left-hand threads, flips asymmetric port layouts, and reverses hardware markings. Flip the panel sequence and text alignment while keeping physical product geometry true to life.

---

## 9. Export Format Selection (SVG / PDF / PNG)

Choose the delivery format that matches your publishing channel—vector print layout, responsive web help center, or support ticket embeds—so thin strokes stay crisp everywhere.

### 9.1 Format Comparison Matrix

| Dimension | SVG (Scalable Vector Graphics) | PDF (Vector Print Document) | PNG (Lossless Raster Image) |
|-----------|-------------------------------|-----------------------------|-----------------------------|
| **Resolution behavior** | Infinitely scalable; compact file size for line art | Preserves vector paths, embedded fonts, and exact physical trim dimensions | Fixed pixel grid; pixelates if scaled above native dimensions |
| **Downstream editability** | High (editable strokes, layers, and `<text>` in Illustrator, Inkscape, Figma, or code) | Medium–High (ideal for press-ready pages and controlled review) | Low (flattened pixels; suitable for final display only) |
| **Best use cases** | Web help centers, HTML docs, reusable template libraries, DTP vector handoff | Offset/digital booklet printing, packaging inserts, archived controlled manuals | Legacy CMS/editors without SVG support, email/chat support snippets, hybrid photo+line figures |

### 9.2 Production Watchouts by Format

- **When exporting SVG**:
  - Always set an explicit `viewBox` attribute (and physical `mm` dimensions such as `width="210mm" height="297mm"` for page templates) so scaling stays deterministic across browsers and DTP tools.
  - Group elements semantically with `<g id="...">` (`header`, `main-figure`, `callouts`, `captions`) for fast editing.
  - Use a universal sans-serif font stack on editable templates, and save an outlined-text (`Convert to Path`) copy when sending final press assets to external print vendors.
  - Ensure zero unembedded local `<image xlink:href="...">` dependencies remain.
- **When exporting print PDF**:
  - Output black line art and body text in **single-channel black (`100% K`) or pure grayscale** rather than 4-color rich black, preventing color fringing on sub-`1 pt` strokes if press plates misregister slightly.
  - Embed all font subsets and verify safe margins (`8–10 mm` inside trim) and bleed (`3 mm` where elements touch page edges).
- **When exporting PNG**:
  - Export at **300–600 DPI** at physical print dimensions (`600 DPI` keeps monochrome line art razor-sharp) or at **`2×` display dimensions** for web documentation.
  - **Use an explicit solid white background (`#FFFFFF`)**: Avoid transparent-background black line art PNGs—when a reader opens a help article or email in Dark Mode, pure black strokes on a transparent canvas vanish completely against dark UI backgrounds.

---

## 10. Pre-Release Quality Checklist

Run through this 10-point check before sending manual illustrations to print or publishing online:

- [ ] **One action per step**: Does each numbered panel focus on one primary motion, with distinct sub-motions split or labeled `① / ②`?
- [ ] **Camera continuity**: Is the viewing angle consistent across consecutive steps, with explicit flip icons wherever the assembly turns over?
- [ ] **Micro-detail zoom**: Do features smaller than `3–4 mm` (notches, cam-lock arrows, buckles, polarity keys) have `2×–4×` magnifier callouts?
- [ ] **Stroke hierarchy**: Are outer silhouettes, internal edges, and thin leaders clearly differentiated, with no stroke thinner than `0.35 pt`?
- [ ] **Unambiguous line roles**: Are motion arrows, static item leaders, and dashed explosion axes visually distinct, with white-halo gaps at crossings?
- [ ] **BOM parity**: Do balloon IDs and quantities match 100% across the master BOM, hardware bag codes, and per-step hardware boxes, with zero crossed leaders?
- [ ] **Visible completion state**: Do critical steps show what "properly seated/locked" looks like (flush edge, `CLICK`, lock icon, or check step)?
- [ ] **Point-of-risk safety cues**: Are power lockout, water shut-off, pinch warnings, anti-tip straps, and load limits shown directly on the step where the hazard arises, using `✓ / ✗` symbols alongside any color cues?
- [ ] **Localization & dark-mode safety**: Do text frames include 35%–50% expansion headroom, and do exported PNGs carry a solid light background?
- [ ] **Target-market standard review**: Have all safety pictograms, signal words, and statutory statements been verified against the safety symbol and instruction manual standards applicable to your target market?
