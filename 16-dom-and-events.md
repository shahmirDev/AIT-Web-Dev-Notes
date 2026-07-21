# 16. Events and DOM Basics

**Learning objective:** Get a lightweight introduction to the DOM and handling basic click events.

**Prerequisite:** [15-numbers.md](./15-numbers.md)

## What is the DOM?

- The **Document Object Model** is how the browser represents an HTML page as objects JavaScript can interact with.

## Selecting Elements

```js
document.querySelector("button"); // selects the first <button>
document.querySelector("#myId");  // selects element with id="myId"
document.querySelector(".myClass"); // selects first element with class="myClass"
```

## Handling Click Events

```js
const button = document.querySelector("button");

button.addEventListener("click", () => {
  console.log("Button clicked!");
});
```

## Why This Matters: Event-Driven Programming

- So far your code has run top-to-bottom in order. `addEventListener` introduces a different style: **event-driven programming** — your code sits and waits, and only runs *when something happens* (a click, a keypress, data arriving).
- Like a doorbell: nobody stands at the door all day — it just rings (fires an event) when someone presses it, and you react then. Most real apps (including React, later) are built this way.

### Common Mistakes
- Selecting an element before it exists in the DOM (script runs too early).
- Forgetting `addEventListener` needs a function, not a function call (`onClick()` vs `onClick`).

### Quick Summary
- DOM = JS's interface to HTML elements.
- `querySelector` selects elements.
- `addEventListener("click", fn)` handles clicks.

*Note: This is intentionally lightweight — advanced DOM manipulation is out of scope for this handbook.*

---
**Previous:** [15-numbers.md](./15-numbers.md) | **Next:** [17-error-handling.md](./17-error-handling.md)
