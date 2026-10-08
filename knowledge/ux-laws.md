# UX Laws & Heuristics — Evaluation Rubric

## Decision & choice
- **Hick's Law**: decision time grows with options. Apply: ≤7 nav items, tiered
  pricing (3 options, one highlighted), filters grouped with sensible defaults.
- **Paradox of choice**: too many equal options → abandonment. Curate, recommend.
- **Default effect**: users keep defaults. Set defaults to the best-for-user choice.

## Motor & perception
- **Fitts's Law**: acquisition time = f(distance, size). Apply: primary CTA large and
  in thumb zone on mobile; related actions adjacent; ≥44px targets.
- **Proximity/Gestalt**: spacing communicates grouping — gaps between groups must be
  visibly larger than gaps within groups.
- **Serial position effect**: first/last items remembered — order nav and lists so
  key items sit at the edges.

## Cognition & memory
- **Miller's Law (7±2)**: chunk everything — forms in sections, phone/card numbers
  formatted, content in scannable blocks.
- **Cognitive load**: every element must earn its place; recognition over recall
  (show examples, previews, selected state — don't make users remember).
- **Progressive disclosure**: ask/show minimum first; advanced options behind a step.

## Expectations & trust
- **Jakob's Law**: users expect your site to work like the ones they know. Deviating
  from e-commerce/nav conventions needs overwhelming justification.
- **Aesthetic-usability effect**: polished UI is perceived as more usable — polish
  buys forgiveness, but doesn't fix broken flows.
- **Nielsen #1 Visibility of system status**: loading, saving, sent — always feedback
  <400ms or a spinner/skeleton.
- **Nielsen #3 User control**: back always works, destructive actions undoable or
  confirmed, no forced funnels without exit.
- **Nielsen #5 Error prevention > #9 error recovery**: constrain inputs (pickers,
  masks) before writing better error messages.

## Motivation & flow completion
- **Goal-gradient effect**: motivation rises near completion — show progress bars
  starting partially filled; count steps down.
- **Peak-end rule**: experiences judged by peak + ending — invest in confirmation
  screens, success states, onboarding finales.
- **Zeigarnik effect**: incomplete tasks nag — resumable flows, "continue where you
  left off".

## Speed heuristics for reviews
1. Can a cold visitor state what/for-whom/next-action in 5 seconds?
2. Count clicks/fields to the primary conversion — can any be removed?
3. Is there exactly ONE visually dominant action per screen?
4. Does every state exist: loading, empty, error, success?
5. Would this pattern surprise a user coming from the category leader?
