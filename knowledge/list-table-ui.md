# List/Table UI — search, filter, sort is default, not an extra

Standing rule: any UI that renders a **list, table, grid
or collection view** ships with search, filter and sort controls, adapted to
the specific data and context — not bolted on generically. Applies to every
agent that builds or reviews UI, and to the main session when it does the
work itself.

## What "adapted to the specific case" means
- **Long/free-text list** (e.g. blog posts, contacts) → fuzzy/substring search box.
- **Catalog with attributes** (e.g. products, courses, components) → faceted
  filters (category, status, tags) as chips/checkboxes, not a single dropdown
  hiding everything.
- **Dense data table** (e.g. bookings, invoices, metrics) → per-column sort
  (click header, asc/desc indicator) + column-scoped filter where useful.
- **Small enumerable set** (e.g. 4 nav items, a components index the size of
  the DS) → search/filter can be skipped, but say so explicitly with a reason
  ("N items, static, no controls needed") — silent omission is the failure
  mode this rule fixes, not the absence of controls on a genuinely tiny list.

## Baseline expectations
- Sort: at least one meaningful default order + a way to change it (column
  header click for tables, a sort-by control for cards/lists).
- Filter: matches the data's actual facets — don't invent filters nobody needs,
  don't skip the ones a real user would reach for first.
- Search: debounced, operates on the fields a user actually searches by
  (name/title first, not internal IDs).
- Empty/no-results state is part of the same gate — a filtered-to-zero view
  needs a clear message + a way to clear filters.
- Tokens/a11y still apply: control styling from the DS, keyboard-operable,
  labeled inputs (no placeholder-only labels).

## Where this plugs in
- Builder agents: build the controls as part of the
  component, not a follow-up.
- `design-system-creator`: if the DS doesn't yet have search/filter/sort
  primitives, that's a gap to close, not a reason to skip the pattern.
- `design-reviewer`: reject a shipped list/table with no controls and no
  explicit exemption note (same severity tier as a missing state).
- `ui-frontend-lead` / orchestrator: when scoping a workstream that includes
  a list/table, call this out in the delegation so it isn't discovered late.
