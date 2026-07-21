# 25. Express Basics

**Learning objective:** Build a REST API with Express — the "E" in MERN.

**Prerequisite:** [24-nodejs-basics.md](./24-nodejs-basics.md)

## What is Express?

- A minimal web framework on top of Node's `http` module.
- Handles routing, request/response parsing, and middleware so you don't build it by hand.

### Why This Matters: Layered Architecture

- Back to the restaurant analogy from [01-introduction.md](./01-introduction.md): if Node is the kitchen, Express organizes it into stations — **routes** decide which "station" handles an incoming order, **middleware** are prep steps every order passes through first (like checking an ID before serving alcohol), and later, **models** (MongoDB/Mongoose) are the pantry where ingredients (data) are actually stored.
- Splitting an app into these layers — instead of one giant file doing everything — is a real architectural pattern, and it's why large apps stay manageable as they grow.

## Setup

```bash
npm install express
```

```js
const express = require("express");
const app = express();

app.use(express.json()); // parse JSON request bodies into req.body

app.get("/", (req, res) => {
  res.send("Hello from Express!");
});

app.listen(3000, () => console.log("Server running on port 3000"));
```

## Routing

```js
app.get("/users", (req, res) => res.json([{ id: 1, name: "Alice" }]));
app.get("/users/:id", (req, res) => res.json({ id: req.params.id }));
app.post("/users", (req, res) => res.status(201).json(req.body));
app.put("/users/:id", (req, res) => res.json({ updated: req.params.id }));
app.delete("/users/:id", (req, res) => res.status(204).send());
```

## REST Conventions

- REST is an **architectural style** (a set of agreed conventions, not a library) for designing APIs so any frontend can predictably talk to any backend — same idea as everyone agreeing to drive on the same side of the road.

| Method | Purpose | Typical status |
|---|---|---|
| GET | Read data | 200 |
| POST | Create data | 201 |
| PUT | Replace data | 200 |
| DELETE | Remove data | 204 |

## Middleware

- A function that runs between the request and the response. Order matters — they run top to bottom.

```js
app.use((req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next(); // must call next() or the request hangs
});
```

## Error-Handling Middleware

- Same as regular middleware, but with **four** parameters — Express recognizes it by that signature.

```js
app.use((err, req, res, next) => {
  console.error(err.message);
  res.status(500).json({ error: "Something broke" });
});
```

### Common Mistakes
- Forgetting `express.json()` — `req.body` is `undefined` on POST/PUT requests without it.
- Wrong middleware order — error handlers must go **last**, after all routes.
- Forgetting to call `next()` in middleware — the request hangs forever.
- Not sending a response in a route — the client waits until it times out.

### Quick Summary
- Express = routing + middleware on top of Node's `http`.
- `app.get/post/put/delete` map to REST's read/create/replace/remove.
- Middleware runs in order; error handlers take `(err, req, res, next)` and go last.

---
**Previous:** [24-nodejs-basics.md](./24-nodejs-basics.md) | **Next:** [26-mongodb-and-mongoose.md](./26-mongodb-and-mongoose.md)
