# 22. Async JavaScript

**Learning objective:** Understand callbacks, Promises, async/await, and `fetch` — needed before Node, Express, or React, since all of them do real work asynchronously (files, databases, network requests).

**Prerequisite:** [21-cheat-sheet.md](./21-cheat-sheet.md)

## Why Async?

- JS runs one thing at a time (single-threaded).
- Slow tasks (reading a file, calling an API) don't block the rest of the code — they run in the background and report back later.

### Why This Matters: Execution Models

- "Synchronous" and "asynchronous" are two different **execution models** — two different philosophies for handling work. Synchronous is like a single cashier serving one customer fully before starting the next; asynchronous is like a waiter who takes an order, sends it to the kitchen, and moves on to the next table instead of standing there waiting.
- This is why a server (coming up in Node/Express) can serve thousands of users at once without freezing — it doesn't wait around for slow things like database queries.

## Callbacks

- A function passed to run later, when a task finishes.

```js
setTimeout(() => {
  console.log("Ran after 1 second");
}, 1000);
```

- Deeply nested callbacks ("callback hell") is why Promises exist.

## Promises

- An object representing a value that will exist **eventually**. Three states: `pending`, `fulfilled`, `rejected`.

```js
function getUser() {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve({ name: "Alice" }), 1000);
  });
}

getUser()
  .then(user => console.log(user.name))
  .catch(err => console.log("Failed:", err))
  .finally(() => console.log("Done"));
```

## Async / Await

- Cleaner syntax for working with Promises. `await` pauses the function until the Promise resolves.

```js
async function loadUser() {
  try {
    const user = await getUser();
    console.log(user.name);
  } catch (err) {
    console.log("Failed:", err);
  }
}
```

- `await` only works inside an `async` function.

## Fetch API

- Built-in way to make network requests (calling an API).

```js
async function loadPosts() {
  const response = await fetch("https://api.example.com/posts");
  const data = await response.json();
  console.log(data);
}
```

### Common Mistakes
- Forgetting `await` — you get a Promise object instead of the actual value.
- Not wrapping `await` in `try/catch` — a rejected Promise crashes the function silently.
- Forgetting `fetch` doesn't reject on HTTP errors (404/500) — only on network failure. Check `response.ok` if you need to catch those.

### Quick Summary
- Callbacks → old way, leads to nesting.
- Promises → `.then()/.catch()/.finally()`.
- Async/await → Promises with normal-looking code; use `try/catch` for errors.
- `fetch()` → make network requests, always `await` twice (the response, then `.json()`).

---
**Previous:** [21-cheat-sheet.md](./21-cheat-sheet.md) | **Next:** [23-npm-and-modules.md](./23-npm-and-modules.md)
