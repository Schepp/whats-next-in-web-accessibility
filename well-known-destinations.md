## Well Known Destinations

---

Many websites use different labels and placements for common navigation targets like “About Us”, “Login” or “Contact”.  

This inconsistency can be disorienting — especially for people with cognitive impairments.

---

### Concept: Standardized rel-Attributes for Navigation

The WAI-Adapt Task Force proposes using standardized `rel` values on `<a>` elements to signal the intent of links.

```html
<a href="/about" rel="about-us">About us</a>
<a href="/login" rel="login">Log in</a>
<a href="/help" rel="support">Help</a>
```

These attributes can provide semantic clarity for assistive technologies.

---

Another possibility is to place redirects at `.well-known` URLs:

* `/.well-known/ia/contact`
* `/.well-known/ia/home`
* `/.well-known/ia/log-in`
* `/.well-known/ia/search`

Extends the idea of having crawler-discoverable URLs: 

* `/.well-known/change-password`

[A Well-Known URL for Changing Passwords](https://www.w3.org/TR/change-password-url/)

---

### Implementation Status

- This proposal is still **in discussion phase**.
- No browser or assistive technology has implemented support yet.
- Early feedback from previous similar efforts (e.g. XLink roles, rel=prev/next) warns about:
  - Lack of uptake from browser vendors
  - Limited incentives for developers

---

![Screenshot of a browser extension popup titled "Welcome to ACME Inc. - ACME D...". The popup lists “Site destinations” and includes six large, labeled buttons with icons: 🏠 Home, ♿ Accessibility statement, ☎️ Contact, ❓ Help, 🔒 Log in, and 🛒 Products. The extension appears over a dark-themed ACME Inc. website.](images/extension.png)

[Demo extension](https://github.com/SamsungInternet/wkd-prototype)

---

### Resources

[WAI-Adapt: Well-known destinations Explainer](https://github.com/w3c/adapt/blob/main/explainers/well-known-destinations.md)