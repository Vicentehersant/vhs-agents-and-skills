# Layouts & grid systems canon

Owned/grown by `style-curator` — special-depth area. Each entry: structure ·
characteristics · when to use · pairs well with (from `styles-taxonomy.md`).

## Swiss / International grid
- **Structure**: strict column grid (commonly 12), consistent gutters, content
  snaps to columns with no exceptions, baseline grid for vertical rhythm
- **Characteristics**: predictable, scannable, feels engineered/considered;
  asymmetric column-spans (e.g. content in cols 2-9) read more sophisticated
  than centered symmetric layouts
- **When to use**: content-heavy sites, editorial, design systems needing a
  rigorous foundation before anything else is decided
- **Pairs with**: Swiss style, Minimalism, Corporate-tech

## Editorial / Magazine grid
- **Structure**: variable column-spans per section (not uniform), type
  hierarchy substitutes for some structural lines, images break out of the
  grid deliberately (full-bleed vs contained as an intentional rhythm)
- **Characteristics**: guides the eye through type-size contrast rather than
  boxes; pull-quotes and captions get their own micro-grid
- **When to use**: long-form content, storytelling sections, case studies,
  blog/article templates
- **Pairs with**: Editorial/Magazine-led, Organic/Handcrafted, Luxury

## Broken grid
- **Structure**: a base grid exists but is intentionally violated — elements
  overlap columns, bleed off-canvas, or sit at an angle against the rhythm
- **Characteristics**: high visual tension, draws attention to the violation
  itself (use for hero moments / one focal disruption, not throughout —
  breaking the grid everywhere just reads as "no grid")
- **When to use**: hero sections, single statement moments, portfolio/creative
  work wanting a signature disruption. Cost: harder to keep responsive/AA-safe
  at breakpoints — needs explicit phone-layout spec, don't leave to the builder
- **Pairs with**: Brutalism, Editorial, Memphis

## Bento grid
- **Structure**: mosaic of variable-size rectangular cells (like a bento box)
  within a shared outer grid — each cell content-fit, no forced uniformity
- **Characteristics**: dense but organized, good for feature-summary sections
  (product capability showcases), each cell independently scannable
- **When to use**: feature grids, capability/pricing comparison sections,
  dashboard summary views. Very common in 2023-25 SaaS marketing pages —
  flag as "default trap" if a project wants differentiation and defaults here
  unexamined
- **Pairs with**: Corporate-tech, Neubrutalism, Minimalism

## Asymmetric grid
- **Structure**: deliberate imbalance — one dominant zone (roughly 60-70% visual
  weight) against smaller supporting zones, no mirrored symmetry
- **Characteristics**: creates a clear focal hierarchy without needing scale
  alone to do it; reads more dynamic than centered layouts
- **When to use**: hero sections needing one clear CTA/image focus, split
  layouts (image+text) wanting to avoid the "50/50 boring split" default
- **Pairs with**: most styles — this is a general-purpose upgrade over
  symmetric layouts, low risk

## Modular scale layout
- **Structure**: spacing AND type sizes derive from one ratio (e.g. 1.25, 1.333,
  golden 1.618) rather than ad-hoc values — the scale IS the grid
- **Characteristics**: guarantees visual harmony across every size without
  manual tuning; pairs naturally with a Tailwind/design-token spacing scale
- **When to use**: design-system foundations (design-system-creator should
  request this from style-curator before finalizing type/spacing tokens),
  any project prioritizing consistency at scale over one-off hero drama
- **Pairs with**: Minimalism, Swiss, Corporate-tech

## Full-bleed / immersive
- **Structure**: content ignores container margins entirely at key moments —
  imagery/video/color spans full viewport width
- **Characteristics**: maximizes impact of hero imagery, breaks monotony
  between contained sections; needs explicit contrast-over-image handling
  (hand to a11y-designer — scrim/gradient-protection technique)
- **When to use**: hero moments, brand-statement sections, luxury/hospitality/
  fashion imagery-led stories
- **Pairs with**: Luxury/Editorial-minimal, Organic, Editorial

## Card grid (uniform)
- **Structure**: strictly uniform card sizes in a responsive N-column grid,
  no variation
- **Characteristics**: the safest, most predictable pattern — very easy to
  build responsively, but the least differentiated. Default for listing pages
  (products, blog index, team) where scannability beats drama
- **When to use**: listing/index pages, anywhere content count is unpredictable
  (grid must gracefully re-flow), catalog/e-commerce
- **Pairs with**: Corporate-tech, Minimalism — deliberately neutral, works with
  almost anything since it's a content-container pattern, not a statement

## Split-screen
- **Structure**: viewport divided into 2 (occasionally 3) full-height zones,
  often one static + one scrolling, or one image + one content column
- **Characteristics**: strong immediate contrast (before/after, product/lifestyle,
  two audiences/two products), works well for landing pages with 2 clear paths
- **When to use**: dual-audience landing pages, comparison moments, hero
  sections pairing a strong image with a strong CTA
- **Pairs with**: Asymmetric grid variant when the split isn't 50/50; pairs
  with most styles

---
Add new entries above this line, keep the same 4-field format (structure ·
characteristics · when to use · pairs with).
