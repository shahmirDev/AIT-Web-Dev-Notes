# 3. Variables and Constants

**Learning objective:** Understand how to declare and use `let` and `const`, and why `var` is avoided.

**Prerequisite:** [02-javascript-syntax.md](./02-javascript-syntax.md)

## let

- Declares a variable that **can be reassigned**.

```js
let age = 25;
age = 26; // allowed
```

## const

- Declares a value that **cannot be reassigned**.

```js
const PI = 3.14159;
```

## Why `var` is Mostly Avoided

| Issue | var | let/const |
|---|---|---|
| Scope | Function-scoped | Block-scoped |
| Redeclaration | Allowed | Not allowed |
| Hoisting behavior | Confusing | Safer |

## Naming Rules

- Must start with a letter, `_`, or `$`.
- Cannot start with a number.
- Cannot use reserved keywords (`let`, `class`, etc.).

## Naming Conventions

- Use camelCase: `firstName`, `totalPrice`.
- Use descriptive names: `userAge` not `x`.

### Common Mistakes
- Trying to reassign a `const`.
- Using `var` out of habit, causing scope bugs.

### Quick Summary
- `let` = reassignable, block-scoped.
- `const` = fixed value, block-scoped.
- Avoid `var`.

---
**Previous:** [02-javascript-syntax.md](./02-javascript-syntax.md) | **Next:** [04-data-types.md](./04-data-types.md)
