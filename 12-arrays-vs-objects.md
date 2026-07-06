=== START: 12-arrays-vs-objects.md ===

# 12. Array vs Object

**Learning objective:** Understand when to use an array versus an object.

**Prerequisite:** [11-objects.md](./11-objects.md)

## Comparison Table

| Aspect | Array | Object |
|---|---|---|
| Structure | Ordered list | Key-value pairs |
| Access | By index (`arr[0]`) | By key (`obj.key`) |
| Use case | Collections of similar items | Structured data about one entity |
| Example | `["apple", "banana"]` | `{ name: "John", age: 25 }` |

## Real Examples

**Use an array when:** storing a list of similar items.
```js
const scores = [90, 85, 78];
```

**Use an object when:** describing one thing with multiple attributes.
```js
const student = { name: "Ali", score: 90 };
```

**Combine them when:** storing a list of structured items.
```js
const students = [
  { name: "Ali", score: 90 },
  { name: "Sara", score: 85 }
];
```

### Common Mistakes
- Using an object when order matters (objects don't guarantee visual/insertion order in older engines' mental model — use arrays for ordered data).

### Quick Summary
- Array → list of similar items, accessed by index.
- Object → single entity with named properties.

---
**Previous:** [11-objects.md](./11-objects.md) | **Next:** [13-scope.md](./13-scope.md)

=== END: 12-arrays-vs-objects.md ===
