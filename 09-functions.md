=== START: 09-functions.md ===

# 9. Functions

**Learning objective:** Learn how to create reusable blocks of logic using functions and arrow functions.

**Prerequisite:** [08-loops.md](./08-loops.md)

## Function Declaration

```js
function greet(name) {
  return `Hello ${name}`;
}
```

## Parameters and Arguments

- **Parameter:** placeholder in the function definition (`name`).
- **Argument:** actual value passed when calling (`"Alice"`).

```js
greet("Alice"); // "Alice" is the argument
```

## Return Values

- `return` sends a value back to the caller and ends the function.

```js
function add(a, b) {
  return a + b;
}
const sum = add(2, 3); // 5
```

## Arrow Functions

- Shorter syntax, commonly used for simple functions.

```js
const greet = name => `Hello ${name}`;
```

**Pseudocode for reusable logic:**
```
FUNCTION calculateTotal(price, tax)
  RETURN price + (price * tax)
```

### Common Mistakes
- Forgetting `return` (function outputs `undefined`).
- Confusing parameters and arguments.

### Quick Summary
- Functions bundle reusable logic.
- `return` sends back a result.
- Arrow functions = concise syntax for simple functions.

---
**Previous:** [08-loops.md](./08-loops.md) | **Next:** [10-arrays.md](./10-arrays.md)

=== END: 09-functions.md ===
