# 14. String Basics

**Learning objective:** Learn how to combine and manipulate text using strings.

**Prerequisite:** [13-scope.md](./13-scope.md)

## Concatenation

```js
const first = "John";
const last = "Doe";
const full = first + " " + last; // "John Doe"
```

## Template Literals

- Preferred modern approach; use backticks and `${}`.

```js
const full = `${first} ${last}`; // "John Doe"
```

## Common Methods

| Method | Purpose | Example |
|---|---|---|
| length | Get string length | `"hello".length` → 5 |
| toUpperCase | Convert to uppercase | `"hi".toUpperCase()` → "HI" |
| toLowerCase | Convert to lowercase | `"HI".toLowerCase()` → "hi" |
| trim | Remove whitespace | `"  hi  ".trim()` → "hi" |

### Common Mistakes
- Using `+` concatenation for complex strings instead of cleaner template literals.
- Forgetting strings are immutable (`str[0] = "x"` doesn't work).

### Quick Summary
- Prefer template literals (`` `${var}` ``) over `+` concatenation.
- Key methods: `length`, `toUpperCase`, `toLowerCase`, `trim`.

---
**Previous:** [13-scope.md](./13-scope.md) | **Next:** [15-numbers.md](./15-numbers.md)
