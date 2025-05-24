## Invoker Commands

---

### What Are Invoker Commands?

Invoker commands are a proposed mechanism to **declaratively define which UI element triggers which behavior or updates** in a web application.

---

```html
<button id="mybutton" onclick="window.mydialog.showModal()" 
        aria-controls="mydialog"
        aria-expanded="false" 
        aria-haspopup="dialog">Show modal dialog</button>

<dialog id="mydialog" aria-label="Exemplary dialog">
    <button onclick="window.mydialog.close(); window.mybutton.focus()"
            aria-controls="mydialog"
            aria-expanded="false">Close</button>
    Dialog Content
</dialog>
```

```html
<button commandfor="mydialog" command="show-modal">Show modal dialog</button>

<dialog id="mydialog" aria-label="Exemplary dialog">
    <button commandfor="mydialog" command="close">Close</button>
    Dialog Content
</dialog>
```

<button commandfor="mydialog" command="show-modal">Show modal dialog</button>

<dialog id="mydialog" aria-label="Exemplary dialog">
    <button commandfor="mydialog" command="close">Close</button>
    Dialog Content
</dialog>


---

### Accessibility Benefits

- easier to communicate **cause and effect** relationships in complex UIs
- easier to prevent programming mistakes

---

### Resources

- [Open UI Invoker Commands Explainer](https://open-ui.org/components/interest-invokers.explainer/)
- [Everything you need to know about Invoker Commands - Keith Cirkel](https://www.youtube.com/watch?v=svS_lf9AXkc)