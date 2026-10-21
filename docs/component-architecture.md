# Component architecture

A **block** is a meaningful independent component, not every wrapper element. An **element** belongs to a block. A nested
reusable component becomes its own block, rather than inheriting the parent's name.

```html
<section class="court-agenda">
  <h2 class="court-agenda__title">Upcoming appearances</h2>
  <article class="court-appearance">
    <span class="court-appearance__defendant">Example Defendant</span>
  </article>
</section>
```

Use block boundaries based on reuse, responsibility, and behavior—not only on markup depth. A component may contain 
another block without making that block its element.

For authored markup, direct class selectors usually make ownership clear. For rich text or CMS-generated markup, a single
scoped block with `:where()` element selectors can be clearer than adding classes to every paragraph.
