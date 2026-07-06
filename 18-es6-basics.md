# 18. Introduction to ES6 Features

**Learning objective:** Get a concise overview of the key modern (ES6+) syntax features used throughout this handbook.

**Prerequisite:** [17-error-handling.md](./17-error-handling.md)

## let / const

- See [03-variables-and-constants.md](./03-variables-and-constants.md) for full details.

## Template Literals

- See [14-strings.md](./14-strings.md) for full details.

## Arrow Functions

- See [09-functions.md](./09-functions.md) for full details.

## Destructuring

- Extract values from arrays/objects into variables.

```js
const user = { name: "Alice", age: 25 };
const { name, age } = user;

const nums = [1, 2, 3];
const [first, second] = nums;
```

## Spread Operator

- Expands arrays/objects into individual elements.

```js
const nums = [1, 2, 3];
const moreNums = [...nums, 4, 5]; // [1,2,3,4,5]

const user = { name: "Alice" };
const updatedUser = { ...user, age: 26 }; // { name: "Alice", age: 26 }
```

### Common Mistakes
- Destructuring a key that doesn't exist (results in `undefined`, not an error).
- Forgetting spread creates a **shallow copy**, not a deep copy.

### Quick Summary
- Destructuring: pull values out of arrays/objects easily.
- Spread (`...`): expand/copy arrays and objects.

---
**Previous:** [17-error-handling.md](./17-error-handling.md) | **Next:** [19-mini-project-examples.md](./19-mini-project-examples.md)
