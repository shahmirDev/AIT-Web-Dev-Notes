# 13. Scope

**Learning objective:** Understand global, function, and block scope in JavaScript.

**Prerequisite:** [12-arrays-vs-objects.md](./12-arrays-vs-objects.md)

## Global Scope

- Declared outside any function/block; accessible everywhere.

```js
const appName = "MyApp"; // global

function show() {
  console.log(appName); // accessible here
}
```

## Function Scope

- Variables declared inside a function are only accessible within it.

```js
function greet() {
  const message = "Hi"; // function-scoped
  console.log(message);
}
// message is not accessible outside greet()
```

## Block Scope

- `let` and `const` are scoped to `{ }` blocks (if, for, while, etc).

```js
if (true) {
  let blockVar = "inside";
  console.log(blockVar); // works
}
// blockVar is not accessible here
```

### Common Mistakes
- Expecting `let`/`const` declared in a block to be usable outside it.
- Overusing global variables, causing naming conflicts (see [03-variables-and-constants.md](./03-variables-and-constants.md)).

### Why This Matters: Encapsulation

- Keeping a variable contained to where it's needed (instead of making everything global) is the seed of a bigger software design idea called **encapsulation** — bundling data so only the right parts of your code can touch it.
- Like a locker: you don't want every stranger reaching into it, only the code that actually needs that variable.

### Quick Summary
- Global scope: accessible everywhere.
- Function scope: accessible only inside that function.
- Block scope: accessible only inside `{ }` (with `let`/`const`).

---
**Previous:** [12-arrays-vs-objects.md](./12-arrays-vs-objects.md) | **Next:** [14-strings.md](./14-strings.md)
