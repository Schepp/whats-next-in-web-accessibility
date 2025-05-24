## CSS-only Carousels

---

### Carousels Are (Still) Everywhere

Carousels or sliders are common UI patterns on:

- Homepages
- Product galleries
- Testimonials
- News tickers

But… they’re often **inaccessible**.

---

### The Problem

Most carousels:

- Trap keyboard focus
- Don’t announce changes to screen readers
- Are hard to navigate via assistive tech
- Auto-advance without user control

---

### CSS-Only Carousels?

Can we build **accessible** carousels **without JavaScript**?

---

### New CSS Overflow 5 Module Additions

```css
.carousel {
   overflow-x: auto;
   scroll-snap-type: x mandatory;
   scroll-marker-group: after;
   
   > li { scroll-snap-align: center }
   
   &::scroll-button(left) { content: "⬅" / "Scroll Left" }
   
   &::scroll-button(right) { content: "⮕" / "Scroll Right" }
   
   > li::scroll-marker { content: '' }

   > li::scroll-marker:target-current { background: var(--accent) }
}
```

---

### Examples

[Carousel Gallery](https://chrome.dev/carousel/)

---

### Sadly...

They are inaccessible as well!

📝 [sarasoueidan.com/blog/css-carousels-accessibility](https://www.sarasoueidan.com/blog/css-carousels-accessibility/)
