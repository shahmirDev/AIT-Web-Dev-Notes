=== START: 21-cheat-sheet.md ===

# 21. Final Cheat Sheet

**Learning objective:** Quickly review core JavaScript fundamentals before interviews or coding practice.

**Prerequisite:** [20-best-practices.md](./20-best-practices.md)

## Variables

```js
let age = 25;      // reassignable
const PI = 3.14;   // fixed
```

## Data Types

| Type | Example |
|---|---|
| String | `"hi"` |
| Number | `42` |
| Boolean | `true` |
| Undefined | (declared, no value) |
| Null | `null` |
| Object | `{}` |
| Array | `[]` |

## Operators

```js
+ - * / %      // arithmetic
= += -=        // assignment
== === != !==  // comparison (prefer === / !==)
&& || !        // logical
```

## Conditionals

```js
if (cond) { ... } else if (cond2) { ... } else { ... }
switch (val) { case 1: ...; break; default: ... }
const result = cond ? "yes" : "no";
```

## Loops

```js
for (let i = 0; i < n; i++) { ... }
while (cond) { ... }
do { ... } while (cond);
break;    // exit loop
continue; // skip iteration
```

## Functions

```js
function greet(name) { return `Hi ${name}`; }
const greet = name => `Hi ${name}`;
```

## Arrays

```js
const arr = [1, 2, 3];
arr.push(4); arr.pop();
arr.shift(); arr.unshift(0);
arr.includes(2); arr.indexOf(2);
```

## Objects

```js
const obj = { name: "John", age: 25 };
obj.name;      // dot notation
obj["name"];   // bracket notation
```

## Common Methods Quick Reference

| Category | Methods |
|---|---|
| String | `length`, `toUpperCase()`, `toLowerCase()`, `trim()` |
| Number | `parseInt()`, `parseFloat()`, `Math.round/floor/ceil` |
| Array | `push`, `pop`, `shift`, `unshift`, `includes`, `indexOf` |

### Quick Summary
This cheat sheet condenses files 03–11 into a single quick-reference page. For deeper explanations, revisit the linked files throughout this handbook.

---
**Previous:** [20-best-practices.md](./20-best-practices.md) | **Start over:** [01-introduction.md](./01-introduction.md)

=== END: 21-cheat-sheet.md ===
