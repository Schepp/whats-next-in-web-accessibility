## Invoker Commands

---

### What Are Invoker Commands?

Invoker commands are a proposed mechanism to **explicitly define which UI element triggers which behavior or updates** in a web application.

This concept is especially useful for:
- Disambiguating multiple buttons or controls that affect a shared region
- Making assistive technology interaction more predictable and explainable

---

### Concept Example

```html
<button id="add-to-cart" invoker-command="add-to-cart">
  Add to cart
</button>

<div id="cart" command-target="add-to-cart">
  <!-- Updated cart preview -->
</div>
```

Screen readers could announce:
> “Add to cart, affects cart preview.”

---

### Accessibility Benefits

- Helps users understand **cause and effect** relationships in complex UIs
- Improves support for **assistive automation tools**
- Makes keyboard-only and voice interaction more transparent

---

### Implementation Status

- Still under discussion in WAI-ARIA and related W3C groups
- Requires collaboration with browser vendors and screen reader makers
- Potentially complements other features like `aria-controls` or `aria-flowto`

---

### Challenges

- Needs clear specification to avoid confusion with similar attributes
- Screen readers must implement logic to interpret the relationships
- Developers must annotate components with consistency

---

### Further reading

[Use CSS reading-flow for logical sequential focus navigation](https://developer.chrome.com/blog/reading-flow)

