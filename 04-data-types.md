=== START: 04-data-types.md ===

# 4. Data Types

**Learning objective:** Learn JavaScript's core data types and when to use each.

**Prerequisite:** [03-variables-and-constants.md](./03-variables-and-constants.md)

## String

- Text data.

```js
const name = "Alice"; // Use case: storing text like names, messages
```

## Number

- Integers and decimals (no separate "int"/"float").

```js
const price = 19.99; // Use case: calculations, counters
```

## Boolean

- `true` or `false`.

```js
const isLoggedIn = true; // Use case: conditions, flags
```

## Undefined

- A variable declared but not assigned a value.

```js
let score;
console.log(score); // undefined
```

## Null

- Represents "no value" intentionally.

```js
let user = null; // Use case: resetting a value
```

## Object

- Key-value collection.

```js
const car = { brand: "Toyota", year: 2022 }; // Use case: structured data
```

## Array

- Ordered list of values.

```js
const colors = ["red", "green", "blue"]; // Use case: lists of items
```

### Common Mistakes
- Confusing `null` (intentional empty) with `undefined` (not assigned).
- Assuming arrays are a separate "type" — they're actually objects.

### Quick Summary
| Type | Example | Use Case |
|---|---|---|
| String | "hi" | Text |
| Number | 42 | Math |
| Boolean | true | Conditions |
| Undefined | — | Uninitialized |
| Null | null | Empty by choice |
| Object | {} | Structured data |
| Array | [] | Lists |

---
**Previous:** [03-variables-and-constants.md](./03-variables-and-constants.md) | **Next:** [05-operators.md](./05-operators.md)

=== END: 04-data-types.md ===
