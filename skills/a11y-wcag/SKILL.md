---
name: a11y-wcag
description: WCAG 2.2 AA accessibility auditing and fixing — contrast, keyboard, ARIA, forms, motion, touch targets. Use on any UI review, before shipping pages, and whenever accessibility is requested.
---

# A11y / WCAG 2.2 AA

## Audit checklist (ordered by how often it fails in real projects)
1. **Contrast (1.4.3 / 1.4.11)**: text 4.5:1 (3:1 large), UI components and
   borders 3:1. Special cases: text over animated backgrounds/gradients (check the
   worst frame), brand accents used as text (use a darker `-text` token), buttons
   vs page background (may need a distinct surface).
2. **Forms (1.3.1 / 3.3.1 / 4.1.2)**: `<label htmlFor>`, `aria-invalid`,
   `aria-describedby` pointing to the error message, errors as text — not color only.
3. **Keyboard**: full tab order, visible focus (never `outline: none` without a
   replacement), skip link, `tabindex="-1"` on the `<main>` skip target,
   dropdowns/modals trap and restore focus, Escape closes.
4. **Semantics**: landmarks (header/nav/main/footer), heading hierarchy, one h1,
   buttons for actions vs links for navigation, alt text (empty alt for decorative).
5. **Motion (2.3.3)**: respect `prefers-reduced-motion` in every animation — skip
   or reduce the effect, don't just shorten it.
6. **Touch targets**: ≥44×44px on mobile, especially bottom navs and icon buttons.

## Output format
Table: WCAG criterion · element · severity (Critical/Serious/Moderate) · fix with code.
Fix criticals immediately; batch the rest.

## Verification
After fixes: recompute contrast numerically, tab through the page (with a browser
tool if available), confirm the reduced-motion path exists.
