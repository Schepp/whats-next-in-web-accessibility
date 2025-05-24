## Native Exclusive Accordions

---

### Native `<details>` Element

HTML has a built-in element for toggling content visibility:

```html
<details>
  <summary>Question 1</summary>
  <p>Answer 1</p>
</details>
```

<details>
  <summary>Question 1</summary>
  <p>Answer 1</p>
</details>

---

#### Accessibility Benefits

✅ Keyboard accessible  
✅ Focusable summary  
✅ Toggle via Enter or Space  
✅ Automatically exposes expanded content to screen readers
✅ Implicit ARIA  

---

### Exclusive Accordion Behavior

A new browser-supported feature:  
**Only one `<details>` stays open at a time in a group.**

---

#### How To Use It

```html
<details name="exclusive-accordion">
  <summary>One</summary>
  <p>Content One</p>
</details>
<details name="exclusive-accordion">
  <summary>Two</summary>
  <p>Content Two</p>
</details>
```

Give `<details>` the same `name` attribute

---

<div>
  <details name="exclusive-accordion">
    <summary>One</summary>
    <p>Content One</p>
  </details>
  <details name="exclusive-accordion">
    <summary>Two</summary>
    <p>Content Two</p>
  </details>
</div>

When one `<details>` is opened, the others automatically close.

---

New styling possibilities via `::details-content` and `transition-behavior: allow-discrete`

<p class="codepen" data-height="300" data-slug-hash="VwoBQjY" data-pen-title="Styling &amp;lt;details&amp;gt;: Horizontal Accordion (no animation)" data-user="web-dot-dev" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/web-dot-dev/pen/VwoBQjY">
  Styling &lt;details&gt;: Horizontal Accordion (no animation)</a> by web.dev (<a href="https://codepen.io/web-dot-dev">@web-dot-dev</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

---

### Resources

- [Chrome Devs: Exclusive Accordion](https://developer.chrome.com/docs/css-ui/exclusive-accordion)

