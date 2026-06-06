---
name: piceldesigns-frontend-website-designer
description: Use this skill when implementing, refining, or reviewing frontend UI for the Piceldesigns Phase 1 website in Next.js, TypeScript, Tailwind, and Vercel. Trigger for page layout, component styling, responsive behavior, typography, color-system implementation, light/dark theme behavior, CTA presentation, motion restraint, and visual QA against approved design documents. Do not trigger for CMS schema design, backend/API work, analytics setup, architecture changes, or adding pages/sections not already approved.
---

# Piceldesigns Frontend Website Designer

## Context

Execute frontend UI work for the Piceldesigns Phase 1 website, a serious design studio and service business website approved by the Piceldesigns founder.

Assume this project stack: Next.js, TypeScript, Tailwind, Vercel, Sanity, Resend, Cloudflare Turnstile, and Plausible.

Use this as a practical implementation skill. Do not treat it as an open-ended design exploration skill.

## Source Of Truth

Before coding, check the relevant approved documents in this order:

1. Frozen Website Architecture
2. Developer Build Brief v2
3. CMS Schema / Content Model Map Final Locked
4. Website Copy Draft v2.2
5. UI Direction Pack v4

When documents conflict, the higher document wins. Stop and flag the conflict before proceeding if the requested UI change cannot satisfy the approved hierarchy.

If reference files are bundled with this skill, load only the relevant approved document for the current task. Recommended references are:

- `references/ui-direction-pack-v4.md`
- `references/developer-build-brief-v2.md`
- `references/website-copy-draft-v2-2.md`
- `references/frozen-website-architecture.md`

## Locked Rules

Enforce these rules on every UI implementation, refinement, and review:

- Maintain exactly the 12 approved live pages. Do not add blog, FAQ, pricing, industries, insights, or extra pages.
- Use only the core services: Brand Identity Design, Website Design, Visual Systems, and Recurring Creative Support.
- Treat Brand Motion as a supporting capability only. Never present Brand Motion as a standalone service or nav item.
- Keep WhatsApp as the primary CTA.
- Preserve locked CTA labels from the approved copy and build documents. Do not rewrite, shorten, or invent CTA labels.
- Use the approved two-column desktop grid only where approved: homepage selected work, services index cards, service-page related projects, and work / portfolio grid.
- Use one-column layout on mobile for those approved grids.
- Keep the default theme white.
- Support dark mode through system preference only. Do not add a manual dark mode toggle.
- Use CSS custom properties for theme colors.
- Do not hardcode hex values in components.
- Use red `#CC0000` only for form validation and error messaging.
- Keep the footer dark in all themes.
- Render nothing for empty-state sections with missing CMS content. Do not render empty wrappers, headings, cards, or spacing shells.
- Do not add carousels, auto-advancing sliders, letter-by-letter animation, or scroll hijacking.
- Do not ship placeholder content in production.

## Workflow

1. Identify the exact page, section, or component being changed.
2. Check the relevant approved documents before coding. Use the hierarchy above to resolve structure, copy, layout, and visual direction.
3. Confirm whether the work affects layout, copy boundaries, CTA rules, theme rules, responsive behavior, CMS-editable fields, or code-controlled structure.
4. Implement the smallest correct change that satisfies the approved documents.
5. Prefer updating existing components, tokens, and patterns over creating new variants.
6. Preserve code-controlled versus CMS-editable boundaries. Do not expose structural controls in Sanity unless the approved CMS model already allows them.
7. Verify the result against the locked UI rules.
8. Run or recommend relevant QA checks before considering the task done.

Ask for clarification instead of improvising when a UI decision is ambiguous. Stop and flag any conflict with the approved documents before proceeding.

## Implementation Guidance

Keep implementation minimal, polished, and production-ready:

- Follow existing project conventions for Next.js routes, TypeScript types, Tailwind utilities, shared components, CMS data access, and theme tokens.
- Keep approved structure intact. Do not use implementation work as a reason to redesign the page or create unapproved sections.
- Keep copy ownership clear. Use approved static copy where the documents lock copy; use CMS fields only where the content model makes that content editable.
- Use semantic CSS variables and Tailwind token mappings for colors, surfaces, text, borders, focus states, and theme behavior.
- Keep components visually restrained. Motion should support clarity and polish, never become a showpiece.
- Keep layouts responsive with explicit constraints so text, CTAs, cards, and media do not overlap or reflow unpredictably.
- Ensure all conditional CMS-driven sections return `null` when the required content is absent.
- Treat visual QA against UI Direction Pack v4 as required, not optional.

## QA Checks

Run the most relevant checks available in the project:

- Type checking for TypeScript changes.
- Linting for code quality and framework rules.
- Unit or component tests when the changed area has existing tests.
- Production build checks when layout, route, theme, or data behavior changes.
- Browser verification for affected pages at mobile and desktop widths.
- Visual inspection of light mode, system dark mode, footer, CTAs, and approved grids.

If a check cannot be run, state that clearly and recommend the exact check to run.

## Done When

Consider the task done only when:

- Layout matches the approved structure.
- Approved desktop grids remain two-column.
- Approved mobile grids remain one-column.
- CTA labels remain locked.
- WhatsApp remains the primary CTA.
- Theme behavior matches white-default plus system-preference dark mode.
- No manual dark mode toggle exists.
- CSS custom properties drive theme colors.
- Red appears only in form validation and error messaging.
- Empty CMS content renders no empty containers.
- Footer remains dark.
- No visual drift from UI Direction Pack v4 is introduced.
- No placeholder content ships in production paths.
- Implementation is production-ready, not prototype-quality.

## Do Not

- Do not add new pages.
- Do not add new sections.
- Do not add new service cards.
- Do not add blog, FAQ, pricing, industries, or insights surfaces.
- Do not turn Brand Motion into a standalone service or nav item.
- Do not change CTA labels.
- Do not replace WhatsApp as the primary CTA.
- Do not expose structural controls in Sanity.
- Do not redesign the product during implementation.
- Do not add new dependencies or UI libraries without approval.
- Do not hardcode colors instead of using semantic tokens and CSS variables.
- Do not add manual theme controls.
- Do not add carousels, auto-advancing sliders, letter-by-letter animation, or scroll hijacking.
- Do not ship placeholder content.
