---
name: deep-research
description: Structured deep research producing numbered, sourced reports in the project's research/ folder — competitors, UX foundations, SEO landscape, color, information architecture, stakeholders, user testing. Use for any investigation that should persist as a document.
---

# Deep Research

## Folder convention
```
research/
├── 00-STATUS-AND-RESUME.md   # handoff: what exists, what's pending
├── 01-<topic>.md             # numbered reports
├── 02-<topic>.md
└── README.md                 # index with a one-line summary per report
```

## Report structure
1. **Objective** — the decision this research must inform
2. **Methodology** — sources, queries, tools used
3. **Findings** — organized by theme, each with a source link
4. **Critical findings** — flagged ⚠️, things that change decisions
   (e.g. "the brand accent fails WCAG AA as text")
5. **Implications for design/code** — concrete and actionable
6. **Recommendation** — one clear recommendation + alternatives considered

## Research types
- **Competitors (direct/indirect)**: positioning, hero patterns, pricing display, IA/nav
- **SEO landscape**: keywords by intent, SERP features, competitor content clusters
- **UX foundations**: user journeys, archetypes, stakeholder maps
- **Visual**: color, typography trends in the niche, reference boards
- **User testing**: script design, tasks, findings synthesis (see `user-testing-synthesis`)

## Rules
- Every claim gets a source. No source → mark it as a hypothesis.
- End every session by updating the status file and the README index.
- Cross-link reports that inform each other.
- Findings that affect the design system get copied into the project CLAUDE.md.
