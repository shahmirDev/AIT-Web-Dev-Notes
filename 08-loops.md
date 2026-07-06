# 8. Loops

**Learning objective:** Learn how to repeat code using `for`, `while`, and `do...while`, plus `break`/`continue`.

**Prerequisite:** [07-conditionals.md](./07-conditionals.md)

## for

**When to use:** Known number of iterations.

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

## while

**When to use:** Unknown number of iterations, condition-based.

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

## do...while

**When to use:** Code must run **at least once** before checking condition.

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

## break

- Exits the loop immediately.

```js
for (let i = 0; i < 10; i++) {
  if (i === 3) break;
  console.log(i);
}
```

## continue

- Skips to the next iteration.

```js
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

## Loop Flowchart

```text
   [ Start ]
       |
  [ Condition? ] --NO--> [ End ]
       |
      YES
       |
  [ Run code block ]
       |
  [ Update counter ]
       |
   (back to Condition)
```

### Common Mistakes
- Infinite loops (forgetting to update the counter).
- Off-by-one errors in loop conditions.

### Quick Summary
| Loop | Best for |
|---|---|
| for | Known iteration count |
| while | Condition-based, unknown count |
| do...while | Must run at least once |

---
**Previous:** [07-conditionals.md](./07-conditionals.md) | **Next:** [09-functions.md](./09-functions.md)
