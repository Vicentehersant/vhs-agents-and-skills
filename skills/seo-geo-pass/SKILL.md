---
name: seo-geo-pass
description: High-level technical SEO + GEO (generative engine optimization for AI search) pass for pages, topic clusters and full sites. Use for audits, new landing pages, blog clusters, schema, sitemaps and AI-citability work.
---

# SEO + GEO Pass

## Scope of a full pass
1. **Technical**: indexability (robots, canonical, sitemap), status codes, Core Web
   Vitals hotspots (LCP image priority, CLS from fonts/animations), semantic HTML, one h1.
2. **On-page**: unique titles/meta, heading hierarchy mirrors search intent,
   internal linking (hub ↔ spoke, guide ↔ money page), alt text, descriptive slugs.
3. **Schema**: JSON-LD for the page type (Organization, LocalBusiness, Service,
   Article, FAQPage, BreadcrumbList, Course/Event). Validate shape.
4. **GEO (AI search)** — make content citable by LLMs:
   - Direct answer in the first 1–2 sentences of each section (extractable)
   - Facts with numbers, dates and named entities
   - FAQ blocks phrased like conversational queries
   - Consistent entity naming (brand, services, locations) across the site
   - llms.txt where appropriate; clean structured data doubles as GEO food
5. **Cluster strategy**: hub page + spokes covering adjacent intents; every spoke
   links the hub + 2–3 siblings; no orphan pages.

## Proven patterns
- **Regulated/certification topics**: pillar hub → per-region subpages →
  "how to navigate X" support guides linking to money pages.
- **Catalogs**: each item gets its own indexable detail page and slug; the
  filterable listing is the hub.
- **Local services**: NAP consistency everywhere + LocalBusiness schema +
  "<service> in <city>" intent landings.

## Output format
Audit table (issue · impact HIGH/MEDIUM/LOW · fix · file) → implement in priority
order → verify the build passes and the sitemap includes new routes.
