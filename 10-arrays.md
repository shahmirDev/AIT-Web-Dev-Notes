# 10. Arrays

**Learning objective:** Learn how to create, access, update, and manipulate arrays.

**Prerequisite:** [09-functions.md](./09-functions.md)

## Why This Matters: Data Structures

- An array is a **data structure** — a way of organizing data so it's easy to work with. Think of it like numbered train carriages: each item has a fixed position (index), and the order is preserved.
- Choosing the right structure (array vs. object, covered next) is a small but real design decision — it shapes how easily you can find, add, or loop through your data later.

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

## Iteration Methods

- These don't change the original array (except `forEach`, which returns nothing). Used constantly in React later.

| Method | Purpose | Example |
|---|---|---|
| forEach | Run code for each item | `arr.forEach(x => console.log(x))` |
| map | Build a new array from each item | `arr.map(x => x * 2)` |
| filter | Keep items that pass a test | `arr.filter(x => x > 2)` |
| reduce | Combine all items into one value | `arr.reduce((sum, x) => sum + x, 0)` |

```js
const nums = [1, 2, 3, 4];

nums.map(n => n * 2);              // [2, 4, 6, 8]
nums.filter(n => n % 2 === 0);     // [2, 4]
nums.reduce((sum, n) => sum + n, 0); // 10
```

### Common Mistakes
- Off-by-one errors (arrays are zero-indexed).
- Confusing `push`/`pop` (end) with `shift`/`unshift` (start).
- Forgetting `map`/`filter` return a **new** array — the original is untouched.
- Forgetting the starting value in `reduce` (the `0` above) — it defaults to the first item otherwise.

### Quick Summary
- Arrays store ordered lists, indexed from 0.
- `push`/`pop` work at the end, `shift`/`unshift` at the start.
- `map` transforms, `filter` selects, `reduce` combines — the three you'll use most in real projects.

---
**Previous:** [09-functions.md](./09-functions.md) | **Next:** [11-objects.md](./11-objects.md)
