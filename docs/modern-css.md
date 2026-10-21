# Modern CSS in Temper

Use the platform when it makes code simpler:

- **Native state:** `:disabled`, `:focus-visible`, `[aria-expanded="true"]`, `[hidden]`; keep semantics in the DOM.
- **Custom properties:** reusable tokens and component-local variation without class proliferation.
- **Grid and Flexbox:** primary layout tools.
- **Logical properties:** `margin-inline`, `padding-block`, etc., when appropriate.
- **Container queries:** components adapting to available space rather than only viewport size.
- **`:where()` and `:is()`:** targeted readability and specificity control.
- **Cascade layers:** only with a documented, project-wide layer order; do not create competing layer orders ad hoc.

Check the project's supported browser baseline before adopting a feature. Don't add modern CSS features just to demonstrate that they exist.

```scss
.article-content :where(p, ul, ol) {
  margin-block: 0 1rem;
}

.accordion__panel[hidden] {
  display: none;
}
```

Avoid using CSS alone to express state that should also be available to assistive technology. Preserve visible keyboard 
focus and respect reduced-motion preferences.
