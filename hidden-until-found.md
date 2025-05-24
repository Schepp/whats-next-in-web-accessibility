## Discoverable Hidden Content

---

#### The Problem

`display: none` or `visibility: hidden` prevent text from being matched in Find-in-Page.

---

### `hidden="until-found"`

A proposed HTML attribute that hides content **until discovered** via the browser’s Find-in-Page (⌘+F / Ctrl+F)

```html
<div hidden="until-found">Glossary Term: A11Y</div>
```

<div hidden="until-found">Glossary Term: A11Y</div>

---

#### Use Cases

- Filtered content (e.g. collapsed tables)
- Deferred sections in long documents  
- Search-matchable but initially hidden terms (accordions)

---

#### Accessibility Benefits

✅ Exposed during search  
✅ Triggered without JS  
✅ Honors focus and scroll behavior  
✅ Works for screen readers and sighted users

---

### Bonus Trick

Make icon-only links findable: https://workingdraft.de

```html
<a href="https://podcasts.social/@workingdraft" aria-label="Mastodon">
  <svg>...</svg> 
  <span hidden="until-found">Mastodon</span>
</a>
```

---

### Resources

- [Making collapsed content accessible with hidden=until-found](https://developer.chrome.com/docs/css-ui/hidden-until-found)
- [Bonus Trick Article](https://schepp.dev/posts/rethinking-find-in-page-accessibility-making-hidden-text-work-for-everyone/)
