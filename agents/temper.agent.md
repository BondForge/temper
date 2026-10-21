# Temper — Coding agent implementation guide

**Purpose:** Implement Temper-compatible CSS/SCSS in the host project. Temper is a BEM-inspired architecture, not a CSS framework.

## Required by default

1. Name authored component classes `block`, `block__element`, `block--modifier`, or sparingly `block__element--modifier` in lowercase kebab-case.
2. Never chain `__` to encode DOM ancestry. `card__header__title` is not acceptable.
3. Use meaningful independent blocks; reusable nested components get their own block.
4. Keep base classes and express independent modifiers separately: `card card--compact card--featured`.
5. Prefer semantic modifiers over implementation detail.
6. Keep selectors shallow; avoid styling IDs, deep descendant selectors, and routine `!important`.
7. Prefer semantic HTML and native state selectors when appropriate; preserve ARIA and keyboard accessibility.
8. Reuse existing tokens and repository conventions; do not invent a token catalog or SCSS structure.
9. Use only centrally defined, approved `u-` utilities; do not invent utilities without review.
10. Do not introduce Tailwind or a competing styling methodology without an explicit architecture decision.

## Preferred techniques, when appropriate

Use CSS custom properties, Grid/Flexbox, logical properties, container queries, `:where()`, `:is()`, and project-wide cascade layers. Check browser support and project conventions. SCSS nesting must not mirror DOM nesting.

## Exceptions

Scoped tag selectors are permitted for rich text or generated markup where BEM classes would add ceremony. Prefer clarity and document meaningful deviations.

## Before completing a change

- Do component names express responsibility rather than DOM ancestry?
- Are modifiers independent and semantic?
- Is specificity low and the markup accessible?
- Are shared tokens and only approved utilities used?
- Does the code fit the host project's SCSS structure and supported browsers?

See `docs/` and `examples/` for explanations and implementation patterns.
