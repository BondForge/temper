# Anti-patterns

## DOM family trees

**Avoid:** `dashboard__wrapper__content__card__header__title`

**Prefer:** `dashboard__title` or `card__title`, depending on ownership. BEM elements do not concatenate ancestors.

## Modifier novels

**Avoid:** `card--compact--featured--interactive`

**Prefer:** `card card--compact card--featured card--interactive` when those are truly independent variants.

## Styling implementation as semantics

**Avoid:** `alert--red`, `card--padding-left-20` when these merely describe incidental CSS.

**Prefer:** `alert--danger`, `card--compact` where the design role is meaningful.

## Class inflation

Don't attach a BEM class to every `div`, `p`, or `span` just to satisfy a naming ritual. Scoped rich-text styling can be more maintainable.

## Selector warfare

Avoid deep descendants, styling IDs, and routine `!important`. Fix ownership, layers, or component boundaries instead.

## Utility cosplay

A dozen one-property utility classes are not a Temper component. Create a meaningful block and stylesheet.
