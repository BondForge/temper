# Temper

**BEM principles. Modern CSS. Less ceremony.**

Temper is an opinionated, BEM-inspired approach to CSS architecture, created and maintained by **BondForge**. It combines
 meaningful component boundaries, predictable class names, modern CSS capabilities, and pragmatic SCSS practices.

**Temper is a methodology, not a framework, package, design system, or runtime dependency.** You can use it with plain 
CSS; our reference examples are SCSS-first because that's what we use.

## Why Temper?

We value BEM's component clarity without turning class names into a transcript of the DOM. We favor semantic names, 
independent blocks, low specificity, native HTML state, and the modern CSS features that simplify implementation. We 
don't require ceremonial classes where scoped selectors are clearer.

Temper isn't an attempt to reinvent CSS or convince the world to adopt our preferred methodology. It's simply how we 
approach CSS architecture at BondForge. We've documented what works for us, why we've made certain decisions, and how 
others can implement the same approach if they find it useful.  If Temper helps another developer or team write clearer, 
more maintainable CSS, then sharing it was worthwhile.  If another approach works better for you, that's great too. Good 
engineering isn't about everyone making the same decisions. It's about making thoughtful decisions that solve the 
problems in front of you.

## Start here

1. Read [the philosophy](docs/philosophy.md).
2. Apply [naming conventions](docs/naming-conventions.md) and [component boundaries](docs/component-architecture.md).
3. Use [SCSS guidance](docs/scss-conventions.md), [modern CSS](docs/modern-css.md), and [controlled utilities](docs/utilities.md).
4. Review [anti-patterns](docs/anti-patterns.md) and the [worked examples](examples/README.md).
5. For coding assistants, use [the agent guide](agents/temper.agent.md).

```html
<article class="case-card case-card--compact">
  <h2 class="case-card__title">Case summary</h2>
  <p class="case-card__description">An example component.</p>
</article>
```

```scss
.case-card {
  --card-gap: 1rem;
  display: grid;
  gap: var(--card-gap);

  &__title { margin: 0; }
  &--compact { --card-gap: .5rem; }
}
```

## Rules at a glance

- Name component classes `block`, `block__element`, `block--modifier` (and sparingly `block__element--modifier`).
- Never chain `__` to mirror DOM ancestry.
- Keep independent modifiers as separate classes alongside the base class.
- Prefer meaningful component boundaries and shallow selectors.
- Use semantic HTML states instead of duplicating them in classes where appropriate.
- Use project design tokens; permit only centrally approved, limited `u-` utilities.
- Prefer simpler modern CSS over historical BEM ceremony when clarity improves.

## Adoption

Copy the conventions into your team's standards and adapt the examples to your tokens, browser support policy, and build 
tooling. You do **not** need to install anything. If you use an AI coding agent, include `agents/temper.agent.md` in its 
project instructions.

## Origin and contribution

Temper originated at BondForge and is shared for anyone to use or adapt. See [CONTRIBUTING.md](CONTRIBUTING.md). Temper 
is not presented as an official extension of the BEM methodology.

## License

Documentation and examples are provided under the [MIT License](LICENSE).
