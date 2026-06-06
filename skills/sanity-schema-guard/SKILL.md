---
name: sanity-schema-guard
description: Use this skill when creating, reviewing, or modifying Sanity CMS schemas for the Piceldesigns Phase 1 website. It protects the boundary between CMS-editable content and fixed website structure. Do not use this skill for general frontend styling, page implementation, deployment, or copywriting.
---

# Sanity Schema Guard

## Purpose

Use this skill to design, review, or modify Sanity schemas for the Piceldesigns Phase 1 website without allowing CMS drift.

Sanity is allowed to manage approved content fields.

Sanity must not control:
- page creation
- page deletion
- route creation
- section ordering
- navigation labels
- navigation order
- CTA hierarchy
- CTA labels where locked
- layout templates
- service creation
- service ordering unless explicitly approved
- unapproved proof claims
- unapproved testimonials
- case study detail pages in Phase 1
- blog, FAQ, pricing, insights, or industries pages

## Source hierarchy

Before schema work, check the approved source documents in this order:

1. Frozen Website Architecture v2.2
2. CMS Schema / Content Model Map Final Locked
3. Developer Execution Brief v3
4. Website Copy Draft v2.2
5. UI Direction Pack v5

If a conflict appears, higher authority wins.

If a required authority document is missing, stop and report the blocker instead of inventing fields.

## Core rule

CMS controls content only.

Code controls:
- routes
- page templates
- fixed section order
- CTA placement rules
- navigation structure
- layout composition
- service page existence
- page count
- Phase 1 exclusions

## Approved schema behavior

Prefer singleton documents for site-wide settings and fixed pages.

Use validation rules for:
- required fields
- approved dropdown values
- approved project categories
- approved service labels
- required alt text where images are exposed
- approved testimonial status
- email format
- URL format
- WhatsApp number/message fields where applicable

Optional fields must degrade cleanly.

If optional content is empty:
- hide the section or content block cleanly
- do not render empty containers
- do not generate fallback filler copy
- do not invent testimonials, client names, numbers, awards, or proof claims

## Required review before schema implementation

Before writing or modifying schema files, produce a Sanity Schema Review Report.

The report must include:

1. Document types proposed
2. Singleton documents proposed
3. Required fields
4. Optional fields
5. Fields intentionally not exposed to editors
6. Validation rules
7. Empty-state behavior
8. CMS boundary risks
9. Questions/blockers
10. Approval needed: Yes/No

Do not implement schema files until approval is given.

## Recommended document types to evaluate

Only propose these if supported by the approved source documents:

- siteSettings
- homepage
- servicePage
- workPage
- aboutPage
- contactPage
- legalPage
- project
- testimonial or trustItem
- globalSeo or seoFields object
- imageWithAlt object
- cta object only where CTA text is not locked by source documents

Do not expose flexible page builders unless explicitly approved.

Do not create generic "sections" arrays that allow editors to reorder or invent layouts.

## Site settings guardrails

siteSettings may contain approved global content such as:
- WhatsApp number
- WhatsApp default message
- inquiry email
- global Open Graph image
- social/profile links if approved
- business contact details if approved

siteSettings must not allow editors to:
- change primary navigation labels
- add navigation items
- change service routes
- create new pages
- change locked CTA labels
- alter footer structure beyond approved editable content

## Project schema guardrails

Project entries may support:
- title
- slug if approved for future Phase 2
- category from approved options only
- summary
- cover image
- alt text
- Behance/external URL for Phase 1
- featured flag
- related service references if approved
- sort order if approved

Phase 1 project cards should link to approved external project URLs, not /work/[slug] detail pages, unless Phase 2 has been approved.

If no project cover image exists, the project card must not render.

## Testimonial / proof guardrails

Testimonials or trust items must include approval control.

Never display unapproved testimonials.

Recommended fields:
- name or client label
- quote or short proof line
- role/company if approved
- approved boolean
- source/context note for internal use
- display location if approved

If no approved proof items exist, hide the proof section entirely.

## Service schema guardrails

Service pages are fixed by code and approved architecture.

Do not allow editors to create new services.

Do not allow editors to rename service routes.

Do not allow editors to reorder service pages unless approved.

Only expose content fields approved by the CMS Schema Map and source documents.

## CTA guardrails

CTA labels are locked where the approved documents define them.

Do not expose locked CTA labels as editable fields.

If CTA fields are exposed, they must be limited to approved destinations or support copy only where source documents allow it.

WhatsApp number and default message should come from siteSettings, with environment fallback where required.

## SEO fields

SEO fields may include:
- meta title
- meta description
- Open Graph title
- Open Graph description
- Open Graph image
- canonical override only if approved

Required:
- every indexable page must have unique metadata
- Thank You page must be noindex
- no keyword stuffing in alt text or metadata

## Output format when invoked

When this skill is used, respond in this format:

### Sanity Schema Guard Report

| Area | Decision | Risk | Action |
|---|---|---|---|

### Proposed document types

### Required fields

### Optional fields

### Fields not exposed to CMS

### Validation rules
