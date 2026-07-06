# 7. Conditional Statements

**Learning objective:** Learn how to make decisions in code using if/else, switch, and ternary operators.

**Prerequisite:** [06-input-and-output.md](./06-input-and-output.md)

## if / else if / else

```js
const age = 20;

if (age >= 18) {
  console.log("Allowed");
} else if (age >= 13) {
  console.log("Teen");
} else {
  console.log("Denied");
}
```

**Pseudocode:**
```
IF age >= 18
  allow access
ELSE
  deny access
```

## switch

```js
const day = "Mon";

switch (day) {
  case "Mon":
    console.log("Start of week");
    break;
  case "Fri":
    console.log("Almost weekend");
    break;
  default:
    console.log("Midweek");
}
```

## Ternary Operator

- Shorthand for simple if/else.

```js
const status = age >= 18 ? "Allowed" : "Denied";
```

## Decision Flowchart

```text
        [ age >= 18? ]
          /       \
        YES        NO
         |          |
    Allow access   Deny access
```

### Common Mistakes
- Forgetting `break` in `switch` (causes fall-through).
- Overusing nested ternaries (hurts readability).

### Quick Summary
- `if/else` → general conditions.
- `switch` → many fixed cases.
- `? :` → short one-line conditions.

---
**Previous:** [06-input-and-output.md](./06-input-and-output.md) | **Next:** [08-loops.md](./08-loops.md)
