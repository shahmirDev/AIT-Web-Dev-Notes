=== START: 15-numbers.md ===

# 15. Number Basics

**Learning objective:** Learn how to parse, round, and work with numbers using the Math object.

**Prerequisite:** [14-strings.md](./14-strings.md)

## Parsing Numbers

- Convert strings to numbers.

```js
parseInt("42");    // 42
parseFloat("3.14"); // 3.14
Number("10");        // 10
```

## Math Object Basics

```js
Math.max(1, 5, 3); // 5
Math.min(1, 5, 3); // 1
Math.abs(-7);      // 7
Math.random();     // random number between 0 and 1
```

## Rounding

```js
Math.round(4.5); // 5
Math.floor(4.9); // 4
Math.ceil(4.1);  // 5
```

### Common Mistakes
- Forgetting `parseInt`/`parseFloat` on user input from `prompt()` (input is always a string).
- Confusing `Math.round`, `Math.floor`, and `Math.ceil`.

### Quick Summary
- Use `parseInt`/`parseFloat`/`Number()` to convert strings to numbers.
- `Math.round/floor/ceil` for rounding.

---
**Previous:** [14-strings.md](./14-strings.md) | **Next:** [16-dom-and-events.md](./16-dom-and-events.md)

=== END: 15-numbers.md ===
