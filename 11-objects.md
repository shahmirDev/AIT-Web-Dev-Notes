=== START: 11-objects.md ===

# 11. Objects

**Learning objective:** Learn how to create objects and access their properties and methods.

**Prerequisite:** [10-arrays.md](./10-arrays.md)

## Creating Objects

```js
const user = {
  name: "John",
  age: 25
};
```

## Properties and Methods

```js
const user = {
  name: "John",
  greet() {
    return `Hi, I'm ${this.name}`;
  }
};
```

## Dot Notation

```js
user.name; // "John"
```

## Bracket Notation

- Useful when property name is dynamic or has special characters.

```js
user["name"]; // "John"
const key = "age";
user[key]; // 25
```

## Real-World Example

```js
const product = {
  title: "Laptop",
  price: 999,
  inStock: true
};
console.log(`${product.title}: $${product.price}`);
```

### Common Mistakes
- Using bracket notation with quotes unnecessarily (`obj["name"]` when `obj.name` works fine).
- Forgetting `this` inside object methods refers to the object itself.

### Quick Summary
- Objects store key-value pairs.
- Use dot notation for known/fixed keys.
- Use bracket notation for dynamic keys.

---
**Previous:** [10-arrays.md](./10-arrays.md) | **Next:** [12-arrays-vs-objects.md](./12-arrays-vs-objects.md)

=== END: 11-objects.md ===
