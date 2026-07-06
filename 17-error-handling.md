# 17. Error Handling Basics

**Learning objective:** Learn the basics of catching errors using `try` and `catch`.

**Prerequisite:** [16-dom-and-events.md](./16-dom-and-events.md)

## try / catch

```js
try {
  const result = 10 / "abc"; // not actually an error in JS, but imagine risky code
  console.log(result);
} catch (error) {
  console.log("Something went wrong:", error.message);
}
```

## A More Realistic Example

```js
try {
  const data = JSON.parse("{ invalid json }");
} catch (error) {
  console.log("Failed to parse JSON:", error.message);
}
```

### Common Mistakes
- Wrapping too much code in one `try` block, making it hard to know what failed.
- Ignoring the caught error instead of logging or handling it.

### Quick Summary
- `try` → code that might fail.
- `catch` → runs if an error occurs, receives the error object.

---
**Previous:** [16-dom-and-events.md](./16-dom-and-events.md) | **Next:** [18-es6-basics.md](./18-es6-basics.md)
