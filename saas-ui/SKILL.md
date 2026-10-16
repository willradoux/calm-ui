---
name: saas-ui
description: Build SaaS interfaces, onboarding, forms and calculators explicitly inspired by AbacatePay's public identity, with lime, dark green, direct Brazilian Portuguese copy and clear operational states. Does not assume the private dashboard layout nor implement payment integration.
---

# SaaS UI

Original skill. The reference is the public identity, not a copy of the authenticated dashboard. Prioritize the task and data readability.

## Visual signature

The public guide uses Fustat for headings and Inter Tight for body text; lime `#9EEA6C`, dark green `#244C4E` and text `#4C5267` are confirmed references. Adapt to the project's brand and font availability. Source: [AbacatePay Design](https://www.abacatepay.com/design).

Reserve lime for actions/surfaces with dark text. Do not use lime or bright green for small text on white without checking contrast. Success/error colors are semantic roles independent of the primary color.

Use the [proposed tokens](assets/tokens.css) as an optional base. They are not the company's official design system. Read [operational recipes](references/operational-patterns.md) for forms, calculators and listings.

## Building

- Use a direct tone in Brazilian Portuguese (pt-BR), persistent labels and specific instructions. Errors should say how to continue; do not joke about financial failures.
- Distinguish presentation from operation. Thin grids, pill CTAs and expressive headings can work in campaigns; lists and tables need their own alignment and density.
- Show consequences next to the choice: result beside the control, summary before confirming, visible filters and an identifiable selected state.
- Preserve precision: currency, dates, sign, rounding and status must match the domain. A visual success indicator only appears when the state known to the application justifies it.
- Do not put every screen inside rounded white cards. Group by task and use dividers/spacing when they are enough.
- Do not reproduce the reference's fees, testimonials, metrics or product availability as facts about the project's service.

## Acceptance

Check labels/errors via keyboard, long monetary values, missing data, filters with no results, recoverable failures and repeated saves. On mobile, the priority is reading and acting: a table may need a scrollable region or a summarized representation with access to details.

Deliver the UI and its states, along with the validations performed. If there is a real payment integration, use the specific documentation in a separate task; this skill does not define financial rules nor verify transactions.
