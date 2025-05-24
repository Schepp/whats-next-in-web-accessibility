## Native Popovers

---

### What is a Popover?

A **popover** is a transient UI element that appears in relation to another element – often for:

- Tooltips
- Dropdown menus
- Off-canvas menus
- Contextual help

---

### Native Popovers in HTML

With the new `popover` attribute, HTML supports native popovers:

```html
<button popovertarget="menu">Open menu</button>

<div id="menu" popover>
  <p>Menu content here</p>
</div>
```

<button popovertarget="menu">Open menu</button>

<div id="menu" popover>
  <p>Menu content here</p>
</div>

(there is also a new `showPopover()` method and a `:popover-open` CSS selector)

---

### Benefits of Native Popovers

✅ Automatically positioned  
✅ Keyboard accessible  
✅ Dismissable via <kbd>Esc</kbd>  
✅ Focus is managed  
✅ Works without JavaScript (in basic cases)

---

### Implicit Accessibility Features

#### 1. Focus Management

- When shown, the popover **receives focus**
- When dismissed, focus returns to the **triggering element**

---

#### 2. Escape to Dismiss

- Popovers are automatically closed when:
  - Pressing <kbd>Esc</kbd>
  - Clicking outside

No extra scripting needed for this.

<button popovertarget="menu2">Open menu</button>

<div id="menu2" popover>
  <p>Menu content here</p>
</div>


---

### Learn More

📖 [developer.chrome.com/docs/html/popover](https://developer.chrome.com/docs/html/popover)

---

### Bonus: `interesttarget`

Opens when The user “shows interest” in an element through various means. For keyboard and mouse users, focusing or hovering the element for a period of time will “show interest”.

```html
<a interesttarget="my-hovercard" href="...">Hover to show the hovercard</a>

<span popover="hint" id="my-hovercard">This is the hovercard</span>
```

---

![Animated GIF showing a button labeled “An interesting button.” When the button is hovered for a moment, a small popup (popover) appears below it with additional content. The popup remains anchored to the button, visually connected, and closes when the button is unhovered again.](images/interest-invoker.gif)

---

### Resources

- [Popover API](https://developer.mozilla.org/en-US/docs/Web/API/Popover_API)
- [Open UI Interest Invoker Explainer](https://open-ui.org/components/interest-invokers.explainer/)