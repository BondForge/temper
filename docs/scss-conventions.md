# SCSS conventions

Temper is CSS-native and **SCSS-first in examples**. Use SCSS for organization and maintainability, not to recreate DOM 
ancestry in selectors.

```scss
.notice {
  padding: var(--notice-padding, 1rem);

  &__title { margin-block: 0; }
  &--compact { --notice-padding: .5rem; }
}
```

Keep nesting shallow. Avoid ID styling, long descendant chains, and routine `!important`. Prefer shared project tokens; 
names in examples are illustrative, not a prescribed token vocabulary. Follow the host repository's stylesheet 
organization, import strategy, formatter, and browser policy.

Use SCSS variables for compile-time concerns when helpful; prefer CSS custom properties for runtime theming and component
variations. Never assume a particular Sass toolchain is required to adopt Temper.
