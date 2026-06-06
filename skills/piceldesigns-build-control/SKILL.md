---
name: piceldesigns-build-control
description: Use this skill whenever working on the Piceldesigns Phase 1 website. It prevents scope drift, protects the approved document hierarchy, and forces planning, implementation, review, and QA to follow the approved build brief before Codex changes pages, components, CMS wiring, theme behavior, navigation, CTAs, analytics, integrations, or responsive frontend behavior.
---

# Piceldesigns Build Control

## Purpose

Control all Piceldesigns Phase 1 website work before planning or coding. Treat this skill as a scope lock, authority check, and implementation gate for the approved build.

Use it before making decisions, proposing implementation, editing files, reviewing code, or running QA for the Piceldesigns Phase 1 website.

## Authority Order

Always check the approved document hierarchy before planning or coding:

1. Frozen Website Architecture v2.2 wins first.
2. CMS Schema / Content Model Map Final Locked wins second.
3. Developer Execution Brief v3 wins third.
4. Copy Draft and UI Direction Pack support only where they do not conflict with the three authority documents above.

If documents conflict, obey the highest-ranking document. If the safe interpretation is not obvious, stop and ask for approval before continuing.

## Pre-Implementation Gate

Before implementation, do all of the following:

- Confirm which source documents are available.
- List missing source documents.
- Produce a source manifest naming each available authority document and its role.
- Produce a build checklist for the requested task.
- Ask for approval if any required authority document is missing.

Do not plan or code around a missing required authority document without explicit approval.

## Scope Locks

Never add or enable:

- Extra pages.
- Blog.
- FAQ.
- Pricing page.
- Insights page.
- Industries page.
- Case study detail pages.
- Standalone Brand Motion service.
- CRM integration.
- Heatmaps.
- Session recording.
- Google Analytics.
- Google Tag Manager.
- Meta Pixel.
- Manual dark mode toggle.

## Build Rules

Enforce these rules on every Piceldesigns Phase 1 task:

- Exactly 12 Phase 1 live pages.
- Four nav items only: Services, Work, About, Contact.
- WhatsApp remains the primary CTA.
- CTA labels must not be rewritten.
- CMS controls content only, not structure.
- Do not hardcode Sanity-controlled values.
- Do not hardcode hex values in components.
- Use CSS variables and Tailwind semantic tokens only.
- Build mobile-first.
- Test 375px, 768px, 1024px, and 1440px in light and dark system modes.

## Ambiguity Protocol

If ambiguity appears:

1. Stop.
2. State the ambiguity plainly.
3. Cite the conflicting or insufficient documents.
4. Propose the smallest safe interpretation.
5. Ask for approval before continuing.

Use this protocol for unclear page counts, nav structure, CTA language, CMS control boundaries, service naming, analytics requests, dark mode behavior, integrations, or any request that may expand scope.

## Operating Workflow

1. Identify the requested page, component, route, CMS field, integration, or QA target.
2. Check the authority documents in order.
3. Produce the required source manifest.
4. Produce the task build checklist.
5. Apply the scope locks and build rules.
6. Determine whether approval is needed.
7. Only then plan, code, review, or run QA.

Prefer the smallest implementation that satisfies the approved documents. Do not redesign, re-architect, or expand the approved build while executing.

## Required Response Format

For every Piceldesigns Phase 1 task, respond using this structure before implementation and when reporting blockers:

```text
Source checked:
- [document names checked, or "Not available"]

Rule applied:
- [specific hierarchy, scope lock, or build rule applied]

Risk/blocker:
- [none, or the ambiguity/missing authority/conflict]

Proposed next action:
- [smallest safe next step]

Approval needed: Yes/No
```

Keep the format brief and concrete. If implementation proceeds after approval is not needed, continue with normal coding updates while preserving these decisions.

## Done When

Consider the work controlled only when:

- The source manifest exists for the task.
- Missing documents are listed.
- Required missing authority documents trigger an approval request.
- Scope locks have been checked.
- Build rules have been checked.
- Any ambiguity has been stopped and escalated.
- The proposed action is the smallest safe interpretation of the approved documents.
