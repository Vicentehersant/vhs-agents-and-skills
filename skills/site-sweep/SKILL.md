---
name: site-sweep
description: Protocol for any "whole site" token/typography change (rename a token, swap a font, change a weight or color everywhere) — enumerate every affected page BEFORE editing, apply to all of them, verify with grep that no raw value survives. Use whenever the request implies "the whole site"/"everywhere", not a single page.
---

# Site Sweep

Failure this fixes: an agent says "done" after fixing one or two pages, and the
user finds the rest still broken page by page.

## Procedure
1. **Enumerate BEFORE editing**: glob/grep every file that can contain the old
   value (page routes, layouts/shared components, CSS/tokens, MDX/content). List
   them as a checklist — this is the scope, not a guess.
2. **Apply to every item**, one by one. Don't skip a page because it "probably"
   already uses the token.
3. **Verify with grep, not eyes**: search the whole affected tree for the old raw
   value (old hex, px, font-family/weight string). Zero hits = done.
4. **Report as a table**: page/file → status (fixed / already correct / N/A).
   Every row from step 1 appears; none silently dropped.

## When unclear, ask
If the scope of "everywhere" is ambiguous (which routes count, shared component
vs page-local override), ask before sweeping rather than under-scoping.
