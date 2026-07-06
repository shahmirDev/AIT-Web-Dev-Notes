# 10. Arrays

**Learning objective:** Learn how to create, access, update, and manipulate arrays.

**Prerequisite:** [09-functions.md](./09-functions.md)

## Creating Arrays

```js
const fruits = ["apple", "banana", "cherry"];
```

## Accessing Elements

```js
fruits[0]; // "apple"
```

## Updating Values

```js
fruits[1] = "mango"; // ["apple", "mango", "cherry"]
```

## Common Methods

| Method | Purpose | Example |
|---|---|---|
| push | Add to end | `fruits.push("kiwi")` |
| pop | Remove from end | `fruits.pop()` |
| shift | Remove from start | `fruits.shift()` |
| unshift | Add to start | `fruits.unshift("grape")` |
| includes | Check existence | `fruits.includes("apple")` |
| indexOf | Find index | `fruits.indexOf("banana")` |

```js
fruits.push("kiwi");     // ["apple","mango","cherry","kiwi"]
fruits.includes("kiwi"); // true
```

### Common Mistakes
- Off-by-one errors (arrays are zero-indexed).
- Confusing `push`/`pop` (end) with `shift`/`unshift` (start).

### Quick Summary
- Arrays store ordered lists, indexed from 0.
- `push`/`pop` work at the end, `shift`/`unshift` at the start.

---
**Previous:** [09-functions.md](./09-functions.md) | **Next:** [11-objects.md](./11-objects.md)
