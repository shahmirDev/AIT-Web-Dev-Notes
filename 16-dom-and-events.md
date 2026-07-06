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
