---
name: design-system-guardian
description: Enforce design-system consistency (tokens, components, spacing, typography, color contrast) whenever styling, creating or reviewing UI. Use before and after any visual change in any project, and for design-system audits.
---

# Design System Guardian

## When to use
Any time UI is created or modified, and explicitly for a design-system audit.

## Procedure
1. **Locate the source of truth** (priority order):
   - Figma variables (via the Figma MCP) if the project has a wired Figma file
   - `globals.css` / `tailwind.config.*` custom properties and theme tokens
   - Project-specific rules in the project CLAUDE.md / design.md (e.g. "brand
     accent only as text via the darker `primary-text` token")
2. **Never hardcode** hex values, px spacing or font sizes if a token exists.
   If no token exists for a needed value, propose adding one — don't inline it.
3. **Reuse before create**: search `src/components/` for an existing component or
   section pattern before building a new one. Match its prop API and naming.
4. **Contrast gate**: every text/background pair passes WCAG AA (4.5:1 normal,
   3:1 large). Compute it, don't eyeball it. For gradients or animated
   backgrounds, check the worst region/frame.
5. **Consistency sweep** after the change: same radius scale, shadow scale,
   spacing rhythm and heading hierarchy as sibling sections.

## Audit output format
Table: element · issue · severity (HIGH/MEDIUM/LOW) · token/component to use · fix.
Ordered by severity, with exact file:line references.

## Red flags to always report
- Two components implementing the same pattern differently
- Inline styles bypassing tokens
- New colors that are near-duplicates of existing tokens (small ΔE)
- Headings skipping levels or multiple h1
- Buttons/links with inconsistent hover/focus states
