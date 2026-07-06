=== START: 02-javascript-syntax.md ===

# 2. JavaScript Syntax

**Learning objective:** Learn the basic building blocks of JS code: statements, semicolons, comments, and formatting rules.

**Prerequisite:** [01-introduction.md](./01-introduction.md)

## Statements

A statement is an instruction the browser executes.

```js
let x = 5;
console.log(x);
```

## Semicolons

- Mark the end of a statement.
- Optional in most cases (ASI - Automatic Semicolon Insertion) but **recommended** for clarity.

```js
let a = 1;
let b = 2;
```

## Comments

```js
// single line comment

/* multi
   line
   comment */
```

## Case Sensitivity

- JS is case-sensitive: `myVar` and `myvar` are different variables.

## Code Formatting

- Use consistent indentation (2 or 4 spaces).
- One statement per line.
- Use blank lines to separate logical blocks.

### Common Mistakes
- Forgetting that `myVar` ≠ `MyVar`.
- Inconsistent semicolon usage causing subtle bugs.

### Quick Summary
- Statements end logically with semicolons.
- Comments: `//` and `/* */`.
- JS is case-sensitive.

---
**Previous:** [01-introduction.md](./01-introduction.md) | **Next:** [03-variables-and-constants.md](./03-variables-and-constants.md)

=== END: 02-javascript-syntax.md ===
