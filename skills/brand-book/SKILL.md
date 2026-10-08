---
name: brand-book
description: Procedure for producing a professional brand book and client brand pack — strategy + visual identity + applications, as a web-based manual and/or PDF, plus the standard deliverables folder. Use when delivering brand documentation.
---

# Brand Book & Brand Pack Production

## Brand book structure (canonical TOC)
1. **Strategy**: essence (one sentence) · values with their functional proof ·
   value pyramid · positioning/onliness · territory · audiences and stakeholders ·
   voice and tone (3 sliders + write-like-this / not-like-this examples)
2. **Visual identity**: logo (construction grid, variants, clearspace in its own
   units, minimum sizes, a MISUSE page with crossed-out examples) · color (full
   specs + 60-30-10 proportions + AA matrix) · typography (families, hierarchy,
   licenses) · imagery (direction + do/don't + prompt system) · iconography ·
   motion (personality, durations, easings)
3. **Applications**: web (link to design.md/docs site) · business cards and
   stationery · email signature · social (profiles, post templates) ·
   presentations · packaging/signage if relevant
4. **Governance**: who approves new uses, how to request assets, changelog

## Format decision
- **Web-based manual** (preferred): built with the project's own design system —
  the manual is the proof. Living document.
- **PDF**: when the client needs an artifact (print vendors, partners). Include
  CMYK swatches and a link to the living version.

## Brand pack folder (client deliverable)
```
brand-pack/
├── 01-logos/       SVG + PNG (1x, 2x) + PDF × variant × RGB/CMYK × positive/negative
├── 02-color/       tokens.css · palette.ase · specs.md
├── 03-typography/  fonts or licenses + specimen.pdf
├── 04-templates/   business card (print-ready, 3mm bleed) · signature.html · social/
├── 05-imagery/     moodboard · prompt-system.md · approved examples
└── README.md       what each thing is + quick rules + contact
```

## Quality gates before delivery
- Logo legible at 16px and in monochrome
- Every color pairing in the AA matrix
- Fonts licensed for the client's actual uses (web + print + social)
- Print files: CMYK, bleed, outlined text or embedded fonts
- Voice examples are real approved copy, not lorem ipsum
- A stranger could apply the brand correctly using ONLY the book (the real test)
