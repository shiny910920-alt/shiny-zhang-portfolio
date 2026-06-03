# Shping — Figma Blueprint

A complete Auto Layout spec to rebuild the Shping case study in Figma.
Light, premium, product-strategy aesthetic (Stripe / Linear / Notion reference).

---

## 0 · Foundations (set these up first)

### Page / artboard
- **Master frame width:** 1440 px (desktop). Mobile variant: 390 px.
- **Layout grid:** 12 columns · 80 px column / 24 px gutter · **side margins 150 px** for standard sections, **50 px** for wide (image) sections.
- **Vertical:** Auto Layout, direction **Vertical**, gap **0** (each section owns its own padding), align **stretch / fill width**.

### Color styles
| Style name | Hex | Use |
|---|---|---|
| `bg/white` | #FFFFFF | Primary background |
| `bg/soft` | #F8F8F8 | Secondary surface |
| `bg/soft-2` | #F2F2F3 | Tertiary surface (centre nodes) |
| `bg/ai` | #F5F6FF | AI band background |
| `text/ink` | #111111 | Primary text |
| `text/body` | #353535 | Body text |
| `text/secondary` | #6B6B6B | Secondary text |
| `text/muted` | #9A9A9A | Captions / eyebrow muted |
| `border/line` | #1111111A (10%) | Dividers / card borders |
| `border/soft` | #1111110F (6%) | Section dividers |
| `accent/pink` | #FF2E63 | Shping brand accent |
| `accent/pink-tint` | #FF2E6312 (7%) | Card hover / icon fill |
| `accent/money` | #12B886 | Value / money emphasis |
| `accent/ai` | #5B6CFF | AI sections emphasis |

### Text styles (Figma text styles)
| Style name | Font | Weight | Size | Line | Tracking | Case |
|---|---|---|---|---|---|---|
| `Display/Hero` | Syne | 800 | 70 | 104% | -3% | — |
| `Heading/H2` | Syne | 800 | 48 | 105% | -3% | — |
| `Heading/H3` | Syne | 800 | 34 | 108% | -2.5% | — |
| `Quote/Insight` | Syne | 800 | 42 | 110% | -2.5% | — |
| `Quote/Pull` | Syne | 700 italic | 28 | 125% | -1% | — |
| `Title/Card` | Syne | 800 | 21 | 108% | -2.5% | — |
| `Title/Node` | Syne | 800 | 22 | 100% | -2% | — |
| `Body/L` | DM Sans | 400 | 16 | 180% | 0 | — |
| `Body/M` | DM Sans | 400 | 15 | 175% | 0 | — |
| `Body/S` | DM Sans | 400 | 14 | 165% | 0 | — |
| `Body/XS` | DM Sans | 400 | 13 | 160% | 0 | — |
| `Eyebrow/Label` | DM Mono | 500 | 10 | 100% | 14% | UPPER |
| `Meta/Mono` | DM Mono | 400 | 10 | 170% | 8% | UPPER |
| `Value/Meta` | Syne | 600 | 15 | 120% | -1% | — |

### Effects
- `shadow/card` — Y 14, Blur 50, #1111110A (8%). Use sparingly, image frames only.
- Corner radius tokens: cards **14**, pills **999**, small tags **8**, icon chips **9**.

---

## Reusable components (build once, instance everywhere)

### Component: Global Nav
- **Frame:** `nav/global` · Width fill (1440) · Auto Layout **Horizontal** · padding **20 / 32** · align **center / space-between** · position **fixed top**.
- Left: Logo text "SZ." — Syne 800, 18px, `text/ink`.
- Right: pill group, Auto Layout Horizontal, gap **8**.
  - Pill "HOME" — bg #CCFF00, text #0A0A0A, radius 999, padding 8/18, Syne 700 12px upper.
  - Pill "ABOUT" — bg #00FF85, same.
  - Pill "CONTACT" — bg #0A0A0A, text #FFFFFF, same.
- ⚠️ Do **not** restyle per project — this is the shared portfolio nav.

### Component: Section Label (eyebrow)
- Auto Layout Horizontal · gap 10 · align center.
- Line: 18 × 1 px rect, fill `accent/pink`.
- Text: `Eyebrow/Label`, fill `accent/pink`. e.g. "02 — UNDERSTANDING THE BUSINESS".

### Component: Section Header block
- Auto Layout **Vertical** · gap 16 · padding **72 / 0 / 40**.
- Children: Section Label → H2 (`Heading/H2`) → Supporting paragraph (`Body/M`, `text/secondary`, max width 600).

### Component: Tag / Chip
- Auto Layout Horizontal · padding 6/13 · radius 999 · border `border/line` · text `Meta/Mono` `text/secondary`.

### Component: Primary Button (outline)
- Padding 15/30 · radius 6 · border 1px `accent/pink` · text Syne 700 12px upper `accent/pink`. Hover = fill pink / text white.

### Component: Footer
- Frame `footer` · Width fill · Auto Layout Horizontal · padding 30/40 · space-between · border-top `border/line`.
- Left: "SZ." logo. Centre: link row (HOME · ABOUT · EMAIL · BEHANCE · LINKEDIN) `Meta/Mono`. Right: "© 2025 Shiny Zhang." `Meta/Mono` `text/muted`.

---

# SECTIONS

---

## Frame: 01 Hero
- **Width:** 1440 · **Min height:** 880
- **Auto Layout:** Vertical · justify **end** (content sits bottom)
- **Padding:** 132 top / 150 sides / 60 bottom
- **Gap:** 44

**Contents (top → bottom):**
1. Back link — "← BACK TO PROJECTS" · `Meta/Mono` · `text/secondary` · margin-bottom 52.
2. Category Label (pill) — "CONSUMER REWARDS · AI PRODUCT DESIGN · 2024–PRESENT" · pink border pill · dot + `Eyebrow/Label`.
3. **Project Title** — `Display/Hero` · max-width 18ch · "Transforming a rewards platform into an **intelligent consumer engagement ecosystem.**" (highlight clause in `accent/pink`).
4. Meta row — Auto Layout Horizontal · gap 48 · wrap · padding-top 34 · border-top `border/line`:
   - Project · Role · Industry · Duration → each = Vertical stack: `Eyebrow/Label`(muted) over `Value/Meta`.
   - Project Summary (right-aligned, push to end) — `Body/M` `text/secondary` max-width 440.

**Image Placeholder:** *(none in hero block — cover lives in 01b)*

---

## Frame: 01b Hero Cover
- **Width:** 1440 · **Auto Layout:** Vertical · padding 0 / 50 / 90 (wide gutters)
- Single image frame, radius 14, border `border/line`, `shadow/card`.

**Image Placeholder:** `Hero Cover — Shping app showcase`
**Recommended size:** **1600 × 686** (≈ 21:9). Source: `Cover.png`.

---

## Frame: 02 Understanding The Business
- **Width:** 1440 · Auto Layout Vertical · padding 0/150/48
- **Gap:** 24

**2a · Section Header** (instance) — Label "02 — UNDERSTANDING THE BUSINESS" · H2 "A two-sided value engine." · paragraph.

**2b · Ecosystem Diagram** — Frame `eco` · Auto Layout **Horizontal** · 3 columns (Fill / Hug / Fill) · radius 16 · border `border/line` · gap 0 (use inner dividers).
- **Left card** `eco-side` — padding 40/36 · Vertical gap 16:
  - `Title/Card` "Consumers" → bullet list (`Body/S`, pink dot bullets) → caption "GIVE: PURCHASING & BEHAVIOURAL DATA" (`Meta/Mono`).
- **Centre node** `eco-mid` — bg `bg/soft-2` · padding 40/32 · Vertical · align center:
  - `Title/Node` "SHPING" (pink) → "← →" arrows (`Meta/Mono` muted) → 2-line mono caption.
- **Right card** — mirror of left: "Brands".

**2c · Value Flow strip** — Frame `value-flow` · Auto Layout Horizontal · 4 equal cells · gap 1 (border bg) · radius 14.
- Each cell padding 26/24, Vertical: `Eyebrow/Label`(pink) → `Title/Card`(small) → `Body/S` muted.
- Cells: INPUT·Behaviour / EXCHANGE·Rewards / OUTPUT·Insight / REVENUE·Campaigns.

**Image Placeholder:** *Diagram is built natively (vector) — no raster needed.*
Optional raster fallback: `Business Ecosystem Diagram` — **1200 × 560**.

---

## Frame: 03 The Challenge
- **Width:** 1440 · Auto Layout **Horizontal** · 2 equal columns · gap 1 (border) · padding 0
- Each column = `ch-block`, Auto Layout Vertical, padding **56 / 48**.

**Left column** (bg white):
- Section Label "03 — THE CHALLENGE" → H3 "Rewarding users isn't the same as engaging them." → 2 × `Body/M` (key word "behaviour" in `text/ink` bold).

**Right column** (bg `bg/soft`):
- Label "WHAT USERS TOLD US" → bullet list (em-dash, pink) of 5 items (`Body/S`).
- **Equation row** — Auto Layout Horizontal gap 16: Pill "Effort required" (pink) · ">" (`accent/pink`, Syne 800 21) · Pill "Perceived reward" (grey).
- Closing `Body/S` muted.

**Image Placeholder:** none (typographic section).

---

## Frame: 04 User Insights
- **Width:** 1440 · Auto Layout Vertical · padding 0/150
- Header block (Label "04 — USER INSIGHTS" · H2 "Three truths that reframed the product.").
- Then **3 × Insight rows**, each: Auto Layout Horizontal · grid **160 / Fill** · gap 44 · padding 56/0 · divider bottom `border/soft`.
  - Left: big index numeral — `Display/Hero` size 45, fill `border/line` faint, with the active digit in `accent/pink`. (e.g. "01", "02", "03").
  - Right (Vertical, gap 18):
    - `Eyebrow/Label`(pink) tag — e.g. "MOTIVATION · VALUE PERCEPTION".
    - **Insight Quote** (`Quote/Insight`) — money words in `accent/money`, emphasis in `accent/pink`.
    - *(Insight 01 only)* Pull quote — `Quote/Pull`, ink, with pink curly quotes — "How much is this actually worth?".
    - Body — `Body/L` `text/body`, max-width 600.

**Image Placeholder:** none (typographic, high-impact).

---

## Frame: 05 Product Strategy
- **Width:** 1440 · Auto Layout Vertical · padding top via header.
- Header block — Label "05 — PRODUCT STRATEGY" · H2 "Five pillars, one behaviour goal." · paragraph.
- **Pillar grid** — Frame `pillars` · Auto Layout (use **Wrap**) · 2 columns · gap 1 (border bg) · top border.
  - Pillar cell — padding **44 / 40** · Vertical gap 12 · bg white (hover = `accent/pink-tint`):
    - `Eyebrow/Label`(pink) "STRATEGY 0X" → `Title/Card` → `Body/S` (`text/secondary`, bold words `text/ink`).
  - Pillars 01–04 are half-width; **Pillar 05 = full width** (span 2 cols) labelled "STRATEGY 05 · THE INFLECTION POINT".

**Image Placeholder:** none.

---

## Frame: 06 Dashboard Transformation
- **Width:** 1440 · Auto Layout Vertical · padding 0/150/90
- Header — Label "06 — DASHBOARD TRANSFORMATION" · H2 "From a wall of information to a guided system." · paragraph.
- **Feature row** — Auto Layout Horizontal · grid **1.05 / 1** · gap 56 · align center.
  - **Left = image** frame (radius 14, border, shadow).
  - **Right = content** Vertical: `fr-kicker` (Syne 700 16) → `Body/M` → checklist (4 items, pink check chips 16×16).

**Image Placeholder:** `Dashboard — guided engagement`
**Recommended size:** **1200 × 900** (4:3) — or device mock **1000 × 1200**.

---

## Frame: 07 Behaviour Design & Daily Tasks
- **Width:** 1440 · Auto Layout Vertical · padding 0/150
- Header — Label "07 — BEHAVIOUR DESIGN & DAILY TASKS" · H2 "Designing the loop, not just the screen." · paragraph.

**7a · Habit Loop** — Frame `loop` · Auto Layout Horizontal · **4 equal steps** · gap 1 (border) · radius 16 · border.
- Each step `loop-step` — padding 32/26 · bg `bg/soft` · Vertical:
  - `Eyebrow/Label`(pink) → `Title/Card`(small) → `Body/S` muted.
  - Between steps place an **arrow connector** "→" (`accent/pink`); last step "↻".
  - Steps: CUE · ACTION · REWARD · INVESTMENT.

**7b · Feature row (flipped)** — Auto Layout Horizontal · grid **1 / 1.05** · gap 56:
- **Left = content** (Label "MOTIVATION SYSTEM" · `fr-title` "Turning chores into a streak worth keeping." · 2 body paras · 4-item checklist).
- **Right = image.**

**Image Placeholder:** `Daily Tasks — guided journey`
**Recommended size:** **1200 × 900** (or device **1000 × 1200**).

---

## Frame: 08 AI Personalisation  *(distinct band)*
- **Width:** 1440 · **Background:** `bg/ai` (#F5F6FF) · border-top 1px `accent/ai` 18%.
- Auto Layout Vertical · padding 0/150 (header) then full-width grid.

**8a · Header** — AI tag pill "◇ AI PRODUCT DESIGN" (violet) → Section Label "08 — AI PERSONALISATION" (violet) → H2 "Meet Shping AI." → paragraph.

**8b · AI Quote** — `Quote/Insight` (smaller, ~37px) · max-width 860 · emphasis in `accent/ai`.

**8c · AI grid** — Auto Layout Horizontal · **3 equal cells** · gap 1 · top+bottom border.
- Each cell padding 40/34 · bg white · Vertical: `Eyebrow/Label`(violet) → `Title/Card` → `Body/S`.
- Cells: RECOMMENDATION · RELEVANCE · COGNITION.

**8d · Closing thesis** — `Body/L` paragraph, max-width 760, key clause in `text/ink`.

**Image Placeholder (optional):** `Shping AI — recommendation surface`
**Recommended size:** **1200 × 760**.

---

## Frame: 09 Stories Feature
- **Width:** 1440 · Auto Layout Vertical · padding 100/150
- **Feature row** — Horizontal · grid **1.05 / 1** · gap 56 · align center.
  - Left = image. Right = content (Label "09 — STORIES FEATURE" · `fr-title` "Participation beyond the transaction." · body · 4-item checklist).

**Image Placeholder:** `Stories — community & content`
**Recommended size:** **1200 × 900**.

---

## Frame: 10 Shping Dashboard Hub  *(B2B)*
- **Width:** 1440 · Auto Layout Vertical · padding 0/150 (header) + wide strip.
- Header — Label "10 — SHPING DASHBOARD HUB" · H2 "The other side of the ecosystem." · paragraph.
- **Value-flow strip** (reuse 02c component) · 4 cells · margin 0/50/90:
  - CAMPAIGNS·Performance / CONSUMERS·Behaviour / PRODUCTS·Engagement / BRANDS·Insight.

**Image Placeholder:** `B2B Analytics Dashboard`
**Recommended size:** **1440 × 810** (16:9, full-bleed-ish) — wide showcase.

---

## Frame: 11 Design System
- **Width:** 1440 · Auto Layout Vertical · padding 0/150 (header).
- Header — Label "11 — DESIGN SYSTEM" · H2 "A system built to move faster." · paragraph.
- **Pillar grid** (reuse 05 component) · 2 columns · 4 cells:
  - SCALABILITY · CONSISTENCY · VELOCITY · ALIGNMENT (each `Eyebrow/Label` → `Title/Card` → `Body/S`).

**Image Placeholder (optional):** `Design System — tokens & components`
**Recommended size:** **1200 × 760** (only if a real artefact exists — otherwise keep native cards).

---

## Frame: 12 Outcomes
- **Width:** 1440 · Auto Layout Vertical · padding 0/150 (header).
- Header — Label "12 — OUTCOMES" · H2 "What changed." · paragraph.
- **Outcomes grid** — Auto Layout (Wrap) · 2 columns · gap 1 · top border.
  - Outcome cell — padding 36/40 · Horizontal · gap 20 · align start:
    - Icon chip 36×36 (radius 9, pink border, `accent/pink-tint` fill, pink 16px line icon).
    - Text Vertical: `Title/Card`(small) → `Body/S` muted.
  - 5 items; **last item full-width** (span 2): "A more scalable ecosystem".
  - Outcomes: Clearer reward understanding · Improved engagement opportunities · Stronger motivation · Better product discoverability · A more scalable ecosystem.

**Image Placeholder:** none (qualitative, no invented metrics).

---

## Frame: 13 Reflection
- **Width:** 1440 · Auto Layout Vertical · padding 90/150 · content max-width **820** (left-aligned column).
- Section Label "13 — REFLECTION" → H2 "Designing systems that pay both sides." → 4 × `Body/L` paragraphs (`text/body`); emphasis terms (behaviour, ecosystem thinking, AI product design, "convert one into the other") in `accent/pink`, weight 500.

**Image Placeholder:** none.

---

## Frame: 14 Next Project
- **Width:** 1440 · Auto Layout Horizontal · padding 96/150 · space-between · align end.
- Left Vertical: `Meta/Mono` "NEXT CASE STUDY" → Next Title `next-title` (Syne 800, ~67px) "ZED Picks — Web3 Racing."
- Right: Primary Button (outline) "VIEW CASE STUDY →".

---

## Frame: 15 Footer
- Reuse `footer` component (see Foundations).

---

## Image Placeholder Summary

| # | Placeholder | Size (px) | Ratio | Notes |
|---|---|---|---|---|
| 01b | Hero Cover | 1600 × 686 | 21:9 | `Cover.png` |
| 06 | Dashboard | 1200 × 900 | 4:3 | or device 1000×1200 |
| 07 | Daily Tasks | 1200 × 900 | 4:3 | flipped row |
| 08 | Shping AI (opt) | 1200 × 760 | 16:10 | optional |
| 09 | Stories | 1200 × 900 | 4:3 | |
| 10 | B2B Dashboard | 1440 × 810 | 16:9 | wide showcase |
| 11 | Design System (opt) | 1200 × 760 | 16:10 | optional |

All other sections are **native vector / type** — no raster images needed.

---

## Build order in Figma (fastest path)
1. Create color + text styles (Foundations).
2. Build the 6 reusable components (nav, section label, section header, tag, button, footer).
3. Make the 1440 page frame · Vertical Auto Layout · stretch.
4. Drop section frames 01 → 15 in order; each section is its own Auto Layout frame with the padding/gap above.
5. Add image placeholder frames (grey fill #F2F2F3 + centred label) at the recommended sizes.
6. Duplicate page → resize to 390 for the mobile variant (all 2-col → 1-col, side padding 24).
