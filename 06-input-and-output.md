=== START: 06-input-and-output.md ===

# 6. User Input and Output

**Learning objective:** Learn how JavaScript displays output and (in browsers) collects simple input.

**Prerequisite:** [05-operators.md](./05-operators.md)

## console.log()

- Prints to the browser/Node.js console. Main tool for debugging.

```js
console.log("Hello, World!");
```

## alert()

- Shows a popup message box (browser only).

```js
alert("Welcome!");
```

## prompt()

- Shows a popup asking for user input (browser only).

```js
const userName = prompt("What is your name?");
console.log(`Hello, ${userName}`);
```

### Common Mistakes
- Relying on `alert()`/`prompt()` in production apps (they block the page and are outdated UX).

### Quick Summary
- `console.log()` → debugging output.
- `alert()` → popup message.
- `prompt()` → popup input.

---
**Previous:** [05-operators.md](./05-operators.md) | **Next:** [07-conditionals.md](./07-conditionals.md)

=== END: 06-input-and-output.md ===
