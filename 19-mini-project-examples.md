# 19. Mini Real-World Examples

**Learning objective:** Apply concepts from earlier files in five small, practical examples.

**Prerequisite:** [18-es6-basics.md](./18-es6-basics.md)

## 1. Calculator

**Goal:** Add two numbers using a function.

```js
function add(a, b) {
  return a + b;
}
console.log(add(4, 5));
```
**Output:** `9`

## 2. Counter

**Goal:** Increment a value using a loop.

```js
let count = 0;
for (let i = 0; i < 3; i++) {
  count++;
}
console.log(count);
```
**Output:** `3`

## 3. Grade Checker

**Goal:** Use conditionals to determine a letter grade.

```js
function getGrade(score) {
  if (score >= 90) return "A";
  else if (score >= 75) return "B";
  else return "C";
}
console.log(getGrade(82));
```
**Output:** `"B"`

## 4. To-Do List Data Structure

**Goal:** Represent a to-do list using an array of objects.

```js
const todos = [
  { task: "Buy milk", done: false },
  { task: "Clean room", done: true }
];
console.log(todos[0].task);
```
**Output:** `"Buy milk"`

## 5. User Profile Object

**Goal:** Represent a user's profile using an object.

```js
const profile = {
  name: "Sara",
  age: 28,
  isActive: true
};
console.log(`${profile.name} is ${profile.age} years old.`);
```
**Output:** `"Sara is 28 years old."`

### Quick Summary
- These examples combine functions, loops, conditionals, arrays, and objects into small practical use cases.

---
**Previous:** [18-es6-basics.md](./18-es6-basics.md) | **Next:** [20-best-practices.md](./20-best-practices.md)
