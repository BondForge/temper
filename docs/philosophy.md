# Philosophy

Temper retains the useful parts of BEM—semantic component names, explicit ownership, predictable variation—without 
treating historical implementation habits as immutable rules.

**Optimize for understandable, maintainable CSS, not methodology purity.**

The naming convention helps identify *what* is being styled. Modern CSS and SCSS help determine *how* it is styled. 
Neither should create needless ceremony.

Temper is intentionally framework-independent: it can be used in SPAs, server-rendered pages, and static sites. It is 
also not a design system: it does not prescribe colors, typography, or component appearance.

## Normative language

- **Required by default:** semantic BEM-style names for authored component classes, no chained element ancestry, independent modifiers, controlled utilities.
- **Preferred where appropriate:** native states, design tokens, logical properties, container queries, low-specificity selectors, and project-wide cascade layers.
- **Exceptions:** scoped rich text, generated markup, and other cases where added classes reduce clarity. Explain substantial deviations during review.

Treat new conventions as engineering decisions supported by real use cases, not as tests of ideological loyalty.
