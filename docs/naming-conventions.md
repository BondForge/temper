# Naming conventions

Use lowercase kebab-case inside names:

| Pattern | Example | Purpose |
| --- | --- | --- |
| `block` | `case-card` | Independently meaningful component |
| `block__element` | `case-card__title` | Element owned by a block |
| `block--modifier` | `case-card--compact` | Semantic variation |
| `block__element--modifier` | `form-field__message--error` | Rare element variation |

Keep the base class when using a modifier: `class="case-card case-card--compact"`.

Multiple independent variants use multiple classes: `class="case-card case-card--compact case-card--featured"`.

Never write `case-card__header__title`: an element name does not encode ancestor elements. Use `case-card__title`, or 
introduce an independent `card-header` block if appropriate.

Prefer `button--danger` to `button--red`, and `card--compact` to `card--padding-8`. Presentational names are acceptable 
only when they genuinely represent a defined design-system variant.

Do not invent an element class for every DOM node. A class should have a meaningful styling or component responsibility.
