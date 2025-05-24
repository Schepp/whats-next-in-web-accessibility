## CSS `reading-flow`

---

### The Problem: Visual ≠ Logical Order

CSS Grid, flexbox, or absolute positioning can cause content to appear **out of order** compared to the DOM.

This disrupts:

- Screen reader navigation
- Copy-paste operations
- Voice control systems

---

### Concept: CSS `reading-flow`

This new CSS property allows authors to **explicitly declare reading order**, independent of layout order.

---

### Example

```html
<div class="box">
  <a href="#">One</a> 
  <a href="#">Two</a>
  <a href="#">Three</a>
</div>
```

```css
.box {
  display: flex;
  flex-direction: row-reverse;
}
```

<div class="box">
 <a href="#">One</a>
 <a href="#">Two</a>
 <a href="#">Three</a>
</div>

---

### The fix

```css
.box {
  reading-flow: flex-visual;
}
```

<div class="box2">
 <a href="#">One</a>
 <a href="#">Two</a>
 <a href="#">Three</a>
</div>

---

### Use Cases

- Dashboards with rearranged content blocks
- Mobile layouts where visual stacking changes
- Educational content with side notes or hints

---

Also possible:

```html
<div class="wrapper">
  <a href="#">Item 1</a>
  <a href="#">Item 2</a>
  <a href="#">Item 3</a>
  <a href="#">Item 4</a>
  <a class="first" href="#">Item 5</a>
</div>
```

```css
.wrapper {
  display: block;
  reading-flow: source-order;
}

.first {
  reading-order: -1;
}
```

<div class="wrapper">
  <a href="#">Item 1</a>
  <a href="#">Item 2</a>
  <a href="#">Item 3</a>
  <a href="#">Item 4</a>
  <a class="first" href="#">Item 5</a>
</div>

---

[Read more on developer.chrome.com](https://developer.chrome.com/blog/reading-flow)
