=== START: 05-operators.md ===

# 5. Operators

**Learning objective:** Learn the main operator categories used for calculations, comparisons, and logic.

**Prerequisite:** [04-data-types.md](./04-data-types.md)

## Arithmetic

```js
5 + 2;  // 7
5 - 2;  // 3
5 * 2;  // 10
5 / 2;  // 2.5
5 % 2;  // 1 (remainder)
```

## Assignment

```js
let x = 5;
x += 2; // x = x + 2 → 7
x -= 1; // 6
```

## Comparison

```js
5 == "5";   // true (loose, checks value only)
5 === "5";  // false (strict, checks value + type)
5 !== 3;    // true
5 > 3;      // true
```

## Logical

```js
true && false; // AND → false
true || false; // OR → true
!true;         // NOT → false
```

## Increment / Decrement

```js
let count = 0;
count++; // 1
count--; // 0
```

### Common Mistakes
- Using `==` instead of `===` (leads to unexpected type coercion).
- Confusing `=` (assignment) with `==`/`===` (comparison).

### Quick Summary
- Arithmetic: `+ - * / %`
- Comparison: prefer `===` and `!==`
- Logical: `&& || !`

---
**Previous:** [04-data-types.md](./04-data-types.md) | **Next:** [06-input-and-output.md](./06-input-and-output.md)

=== END: 05-operators.md ===
