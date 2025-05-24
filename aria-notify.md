## ARIA Notify

---

### Problem: Notifications and Assistive Tech

Dynamic updates like:

- Chat messages
- System alerts
- Timers and toasts

…are not always reliably announced by screen readers.

---

### Why?

- Live regions (`aria-live`) were designed for content updates, not ephemeral notifications
- There's **no standardized way to signal an "alert" event** for assistive technologies

---

### Existing `aria-live`: Not Enough

```html
<div role="status" aria-live="polite">Update here</div>
```

- Works **only if the region is already in the DOM**
- No announcement if the element is added dynamically and removed quickly
- Developers often misuse it in ways AT can’t reliably interpret

---

### Enters `ariaNotify`

A new **imperative API** that gives developers a direct way to send a notification event to assistive tech.

Proposed by Microsoft, Google, Apple, and other W3C ARIA WG members.

---

### The Proposed API

```js
// Dispatch a normal priority notification about a background task status update.
document.ariaNotify("Background task completed", { "priority":"normal" });

// Dispatch a high priority notification that data may be lost.
document.ariaNotify("Unable to save changes, connection lost", { "priority":"high" });
```

This triggers a **platform-native accessibility notification**, just like system-level alerts.

---

### Benefits of `ariaNotify()`

✅ Doesn't require DOM elements  
✅ Doesn't depend on screen reader parsing timing  
✅ Cross-platform behavior through:

- Windows UIA Notification Event
- macOS AXNotification
- Planned integration with Android & iOS

---

### Use Cases

- Toasts and snackbars
- Chat and email message notifications
- Auto-saving or background processing messages
- Screen reader-only alerts without visual UI

---

### Implementation Status

- API is **not yet in browsers**
- Proposal has been published via W3C ARIA WG
- Working across browser vendors and ATs for consistent behavior
- Demo implemented in Microsoft Edge (Origin Trial)

---

### Learn More

- [Microsoft Edge Blog: Creating a more accessible web with `ariaNotify`](https://blogs.windows.com/msedgedev/2025/05/05/creating-a-more-accessible-web-with-aria-notify/)  
- [W3C Breakouts Day 2025: Improving Notification Handling with AriaNotify (video)](https://www.w3.org/2025/03/breakouts-day-2025/recordings/recording-2.html#video)
