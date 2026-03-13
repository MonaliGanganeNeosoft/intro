# CSS Interview Questions and Answers

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

This file gives:

1. Definition
2. Why it is used
3. Short answer for interview
4. Coding example where useful

## Theory Questions and Answers

### 1. What is the CSS box model?

Definition:
The box model describes how every element is made of content, padding, border, and margin.

Why used:
It helps control spacing, layout, and element size.

Interview answer:
The final rendered size of an element depends on content size plus padding, border, and margin.

### 2. What is the difference between `content-box` and `border-box`?

Interview answer:
In `content-box`, width and height apply only to content. In `border-box`, width and height include padding and border, which makes layouts easier to manage.

Example:

```css
* {
  box-sizing: border-box;
}
```

### 3. How does CSS specificity work?

Definition:
Specificity decides which rule wins when multiple selectors target the same element.

Why used:
It determines style priority along with cascade and source order.

Interview answer:
Inline styles are strongest, then IDs, then classes/attributes/pseudo-classes, then element selectors. If specificity is equal, the later rule wins.

### 4. How do inline styles, IDs, classes, attributes, pseudo-classes, and element selectors compare?

Interview answer:
Inline styles have highest priority, IDs are stronger than classes and attributes, and element selectors have the lowest specificity among those common selectors.

### 5. What is the cascade in CSS?

Interview answer:
The cascade is the overall process CSS uses to decide final styles based on origin, importance, specificity, and source order.

### 6. What is the difference between `inherit`, `initial`, `unset`, `revert`, and `revert-layer`?

Interview answer:
`inherit` takes the parent value, `initial` resets to the CSS initial value, `unset` behaves like inherit or initial depending on the property, and `revert` rolls back to an earlier cascade source.

### 7. What is the difference between relative and absolute units?

Interview answer:
Absolute units like `px` are fixed. Relative units like `em`, `rem`, `%`, `vh`, and `vw` depend on another value such as font size or viewport size.

### 8. When should you use `rem`, `em`, `%`, `vh`, `vw`, and `clamp()`?

Interview answer:
Use `rem` for scalable typography and spacing, `em` for component-relative sizing, `%` for flexible layouts, `vh` and `vw` for viewport sizing, and `clamp()` for responsive ranges.

Example:

```css
h1 {
  font-size: clamp(1.5rem, 3vw, 3rem);
}
```

### 9. What is the difference between `position: relative`, `absolute`, `fixed`, and `sticky`?

Interview answer:
`relative` offsets from its normal position, `absolute` positions relative to the nearest positioned ancestor, `fixed` sticks to the viewport, and `sticky` switches between relative and fixed behavior while scrolling.

### 10. How does `z-index` work, and what is a stacking context?

Interview answer:
`z-index` controls layering, but only inside the same stacking context. Properties like `position`, `opacity`, and `transform` can create new stacking contexts.

### 11. What is the difference between Flexbox and Grid?

Interview answer:
Flexbox is mainly one-dimensional for rows or columns. Grid is two-dimensional and ideal for full page or card layouts.

### 12. When would you choose Flexbox over Grid in a real project?

Interview answer:
Use Flexbox for navbars, button groups, alignment, and one-axis layouts. Use Grid for dashboards, cards, and complex two-axis page structures.

### 13. What are pseudo-classes and pseudo-elements?

Interview answer:
Pseudo-classes like `:hover` target element states, while pseudo-elements like `::before` and `::after` style virtual parts of an element.

### 14. What is the difference between `visibility: hidden`, `display: none`, and `opacity: 0`?

Interview answer:
`display: none` removes the element from layout, `visibility: hidden` keeps layout space but hides it, and `opacity: 0` makes it transparent but still interactive unless otherwise changed.

### 15. How do media queries work?

Interview answer:
Media queries apply styles based on conditions like screen width, height, orientation, or user preferences.

Example:

```css
@media (max-width: 768px) {
  .sidebar {
    display: none;
  }
}
```

### 16. What is mobile-first CSS?

Interview answer:
Mobile-first means writing base styles for small screens first and then enhancing for larger screens using `min-width` media queries.

### 17. What are container queries, and why are they useful?

Interview answer:
Container queries allow a component to respond to its own container size instead of the whole viewport, which is very useful in component-based systems.

### 18. What are CSS custom properties, and how do they help in large projects?

Interview answer:
Custom properties are reusable variables like `--primary-color` that improve consistency, theming, and maintainability.

Example:

```css
:root {
  --brand-color: #0d6efd;
}

.button {
  background: var(--brand-color);
}
```

### 19. What is the difference between transitions and animations?

Interview answer:
Transitions animate between two states after a change. Animations can run automatically with multiple keyframes and more control.

### 20. How do you optimize CSS for performance in large applications?

Interview answer:
Keep selectors simple, reduce unused CSS, avoid heavy repaints, use transforms for animation, and standardize architecture to reduce overrides.

### 21. What causes layout thrashing or repaint-heavy UI behavior?

Interview answer:
Frequent DOM reads and writes in loops, expensive box-shadow or filter effects, animating layout properties, and too many forced reflows can hurt performance.

### 22. What are common CSS architecture patterns?

Interview answer:
BEM improves naming consistency, utility-first emphasizes small reusable classes, and approaches like SMACSS or OOCSS focus on scalable structure.

### 23. How do you avoid CSS conflicts in large teams and component-based apps?

Interview answer:
Use consistent naming, component scoping, design tokens, code reviews, and avoid global styles where not needed.

### 24. What is the difference between `overflow: hidden`, `auto`, `scroll`, and `clip`?

Interview answer:
`hidden` clips overflow, `auto` adds scrollbars only if needed, `scroll` always shows scrollbars, and `clip` clips overflow without scrollbars.

### 25. How do `min-width`, `max-width`, `min-content`, `max-content`, and `fit-content` differ?

Interview answer:
They control sizing constraints. `min-width` and `max-width` set explicit limits, while content-based values size elements according to content behavior.

### 26. What is the difference between `transform` and changing `top` or `left` for animations?

Interview answer:
Animating `transform` is generally more performant because it avoids layout recalculation and uses the compositor more effectively.

### 27. What CSS features help accessibility?

Interview answer:
Visible focus styles, sufficient color contrast, reduced motion support, readable spacing, and responsive text sizing all improve accessibility.

### 28. How do you support dark mode using CSS?

Interview answer:
Use CSS variables and switch variable values via a class, media query, or theme attribute.

Example:

```css
:root {
  --bg: #ffffff;
  --text: #111111;
}

[data-theme="dark"] {
  --bg: #111111;
  --text: #ffffff;
}

body {
  background: var(--bg);
  color: var(--text);
}
```

### 29. What are logical properties in CSS, and why are they useful?

Interview answer:
Logical properties like `margin-inline` and `padding-block` adapt better to different writing directions and internationalization needs.

### 30. How do you debug a CSS issue in a production UI?

Interview answer:
Inspect the element in dev tools, check computed styles, verify specificity and inheritance, test responsive behavior, and isolate whether layout or state styles are causing the issue.

## Coding and Practical Questions with Answers

### 1. Create a responsive navbar using Flexbox

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
  flex-wrap: wrap;
}
```

### 2. Build a card grid using CSS Grid

```css
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}
```

### 3. Create a two-column layout with sticky sidebar

```css
.layout {
  display: grid;
  grid-template-columns: 280px 1fr;
  gap: 1rem;
}

.sidebar {
  position: sticky;
  top: 1rem;
  align-self: start;
}
```

### 4. Center a modal vertically and horizontally

```css
.modal-overlay {
  position: fixed;
  inset: 0;
  display: grid;
  place-items: center;
}
```

### 5. Build a responsive form layout

```css
.form-row {
  display: grid;
  grid-template-columns: 160px 1fr;
  gap: 0.75rem;
}

@media (max-width: 600px) {
  .form-row {
    grid-template-columns: 1fr;
  }
}
```

### 6. Create a tooltip using only CSS

```css
.tooltip {
  position: relative;
}

.tooltip::after {
  content: attr(data-tip);
  position: absolute;
  left: 50%;
  bottom: calc(100% + 8px);
  transform: translateX(-50%);
  background: #222;
  color: #fff;
  padding: 0.5rem;
  border-radius: 4px;
  opacity: 0;
  pointer-events: none;
}

.tooltip:hover::after,
.tooltip:focus-visible::after {
  opacity: 1;
}
```

### 7. Build a dropdown menu with hover and focus states

```css
.menu {
  position: relative;
}

.menu-list {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
}

.menu:hover .menu-list,
.menu:focus-within .menu-list {
  display: block;
}
```

### 8. Create a loading spinner using CSS animation

```css
.spinner {
  width: 32px;
  height: 32px;
  border: 4px solid #ddd;
  border-top-color: #0d6efd;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}
```

### 9. Implement a dark mode theme using CSS variables

```css
:root {
  --bg: #fff;
  --text: #111;
}

.dark {
  --bg: #111;
  --text: #fff;
}
```

### 10. Make a table responsive for small screens

```css
.table-wrap {
  overflow-x: auto;
}

table {
  min-width: 640px;
}
```

### 11. Create a skeleton loader UI

```css
.skeleton {
  background: linear-gradient(90deg, #eee 25%, #f5f5f5 50%, #eee 75%);
  background-size: 200% 100%;
  animation: shimmer 1.2s infinite;
}

@keyframes shimmer {
  to {
    background-position: -200% 0;
  }
}
```

### 12. Build an accordion style layout with smooth transitions

```css
.accordion-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
}

.accordion-item.open .accordion-content {
  max-height: 200px;
}
```

### 13. Create a reusable button system

```css
.btn {
  padding: 0.75rem 1rem;
  border-radius: 6px;
  border: 1px solid transparent;
  cursor: pointer;
}

.btn-primary {
  background: #0d6efd;
  color: #fff;
}

.btn-secondary {
  background: #fff;
  border-color: #ccc;
}

.btn:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}
```

### 14. Design a pricing section using Grid

```css
.pricing {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}
```

### 15. Fix a layout where long text breaks the design

```css
.card-title,
.table-cell {
  overflow-wrap: anywhere;
}
```

### 16. Create a page layout with header, sidebar, content, and footer

```css
.page {
  min-height: 100vh;
  display: grid;
  grid-template-rows: auto 1fr auto;
}

.main {
  display: grid;
  grid-template-columns: 240px 1fr;
}
```

### 17. Write CSS to truncate text to one line and multiple lines

```css
.one-line {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.multi-line {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
```

### 18. Create a responsive image gallery with equal-height cards

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}

.gallery img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
}
```

## Accenture L2 Style CSS Answers

### 1. How do you structure scalable CSS in a large enterprise application?

Best answer:
Use a clear architecture, shared design tokens, reusable utility patterns, and component-level scoping. Avoid uncontrolled global selectors.

### 2. How do you prevent style leakage across modules or components?

Best answer:
Use CSS Modules, scoped styling, strict naming conventions, and avoid generic global selectors that override unrelated components.

### 3. How would you handle theming for multiple business clients?

Best answer:
Use CSS variables for colors, spacing, and typography, then swap theme tokens through classes, attributes, or client-specific theme files.

### 4. How do you debug a production issue where a component looks correct in Chrome but breaks in Edge?

Best answer:
Check browser support, inspect computed styles, verify layout features used, reproduce with simplified markup, and review fallbacks for newer CSS features.

### 5. What CSS changes improve performance for large dashboards?

Best answer:
Reduce heavy visual effects, avoid layout-triggering animations, simplify selectors, lazy load non-critical styles if needed, and standardize components to reduce override chains.

### 6. How do you create responsive layouts for data-heavy screens?

Best answer:
Use Grid and Flexbox thoughtfully, support horizontal scroll where needed, avoid squeezing complex tables too much, and prioritize readability over forcing everything into tiny columns.

### 7. How do you balance reusable design system classes with component-specific styles?

Best answer:
Use shared tokens and base primitives, but keep truly local rules inside components. Shared styles should solve repeated patterns, not every one-off case.

### 8. When would you use CSS modules, styled-components, Tailwind, or plain SCSS?

Best answer:
It depends on team standards and app architecture. CSS Modules are good for scoped styles, SCSS works well for layered styling systems, styled-components are useful for JS-driven styling, and Tailwind is fast for utility-based consistency.

### 9. How do you review CSS in pull requests for long-term maintainability?

Best answer:
Check naming clarity, reusability, selector complexity, responsive behavior, accessibility, and whether the new styles fit the design system.

### 10. How do you ensure accessibility in focus states, contrast, and reduced motion support?

Best answer:
Never remove focus outlines without a proper replacement, verify contrast ratios, and respect `prefers-reduced-motion` for heavy animations.

## Quick Revision Notes

1. Know box model, specificity, cascade, Flexbox, and Grid very well.
2. Use `border-box` globally in most projects.
3. Prefer `transform` for animations over layout-changing properties.
4. Be confident with responsive design, theming, and scalable CSS architecture.
5. For Accenture L2, focus on maintainability, performance, and enterprise UI scenarios.
