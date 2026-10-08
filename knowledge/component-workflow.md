# Component Workflow — MANDATORY lifecycle for every component/section

Created because of real failure modes: work not documented, Figma components not
updated, gaps and shadows applied off-scale. These steps are NOT optional and
NOT skippable — ui-frontend-lead enforces them as quality gates.

## 1. COMPOSE-FIRST (before creating anything)
Before building a component, CHECK in this order and report what you found:
1. Does an existing component already cover this? → use it
2. Can it be built by COMPOSING smaller existing components/primitives? → compose
3. Do the needed tokens/variables exist (color, spacing, radius, shadow, type)? →
   use them; if one is missing, ADD it to the system (code + Figma variable),
   never inline a value
Creating from zero is the LAST resort and requires stating why nothing composable existed.

## 2. BUILD SPEC (every component ships with ALL of this)
- **Gaps/spacing**: ONLY spacing-scale tokens. Peer elements = equal gaps; group
  separation > intra-group gap (Gestalt). NEVER eyeballed px. Name the tokens used.
- **Shadows**: ONLY the project's shadow scale (sm/md/lg…). No custom one-off
  box-shadows. If the design needs a new elevation, add it to the scale first.
- **States INCLUDING accessibility states — at creation, not later**:
  default · hover · **focus-visible** (visible ring/outline, ≥3:1 vs adjacent,
  never removed) · active · disabled · loading/empty/error where applicable.
  A button without focus-visible is an UNFINISHED component.
- **Responsive**: behavior defined at 375 / 768 / 1280 minimum.

## 3. FIGMA MIRROR (same session, not "later")
When a component/section is created or visually changed:
- Create/update the Figma component (Figma MCP or by hand)
- **Desktop + tablet + phone versions** whenever the layout differs between them
  (if truly identical across breakpoints, note "responsive: single frame" explicitly)
- Variants in Figma mirror the code props (variant/size/state)
- Cannot do it now? → log it in the COMPONENTS INDEX as `figma: PENDING ⚠️`
  — visible debt, never silent omission

## 4. REGISTER in the COMPONENTS INDEX (how other agents find it)
Every project has `docs/components-index.md` (create it if missing):

| Component | Usage (when/how) | Code | Figma | Variants/states | Last edit |
|---|---|---|---|---|---|
| QuoteCard | quote summary inside quote flows; not for static pricing | src/components/quote/QuoteCard.tsx | node 12:340 | default/compact · all states ✓ | 2026-07-12 builder: +compact variant |

Rules: every NEW component gets a row · agents CONSULT this index before building
(it is the map) · missing index row = component doesn't exist for the system.

## 5. TRACK EVERY EDIT (code OR Figma)
Any change to an existing component:
1. Update its row in components-index.md (Last edit: date + who + what)
2. Update its JSDoc/usage docs if the API or usage rules changed
3. Update the Figma counterpart (or mark `figma: PENDING ⚠️`)
4. Significant changes → line in design.md changelog
An edit without its tracking updates is an INCOMPLETE edit — reviewers reject it.

## Definition of "component done"
compose-first check reported · tokens-only gaps/shadows (named) · all states incl.
focus-visible · responsive defined · Figma mirrored (or ⚠️ debt logged) · index row
added/updated · docs current. Six checks — miss one and it's not done.
