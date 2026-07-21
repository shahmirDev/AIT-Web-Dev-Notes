# 30. Putting It Together: The MERN Stack

**Learning objective:** See how MongoDB, Express, React, and Node fit into one project, and where to go after this handbook.

**Prerequisite:** [29-tailwind-css.md](./29-tailwind-css.md)

## What MERN Means

| Letter | Piece | Role |
|---|---|---|
| M | MongoDB | Stores the data |
| E | Express | Backend API (routes, middleware) |
| R | React | Frontend UI |
| N | Node.js | Runs the backend JS |

### Why This Matters: Three-Tier Architecture

- Close the loop on the restaurant analogy from [01-introduction.md](./01-introduction.md): **React** is the dining room (what the customer sees and interacts with), **Express** is the kitchen and waiter (takes orders, prepares responses), and **MongoDB** is the pantry (where everything is actually stored). **Node** is what powers the kitchen equipment.
- This "presentation layer / logic layer / data layer" split is called **three-tier architecture** — a standard shape for most real-world web apps, not just MERN. Once you see it here, you'll recognize it in almost every other stack you meet later.

## Typical Folder Structure

```text
my-app/
├── client/          # React app (Vite/CRA)
│   ├── src/
│   │   ├── components/
│   │   └── App.jsx
│   └── package.json
└── server/          # Express + Mongoose app
    ├── models/       # Mongoose schemas
    ├── routes/       # Express routers
    ├── index.js
    └── package.json
```

- `client` and `server` are two separate Node projects, each with their own `package.json`.

## How a Request Flows

```
React (fetch) → Express route → Mongoose query → MongoDB
                                                      |
React (renders result) <---- JSON response <---------
```

```jsx
// client: React component calls the API
const res = await fetch("/api/users");
const users = await res.json();
```

```js
// server: Express route queries MongoDB via Mongoose
app.get("/api/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});
```

## Environment Variables

- Secrets and config (database URLs, API keys) go in a `.env` file, never hardcoded or committed.

```
// server/.env
MONGO_URI=mongodb://localhost:27017/myapp
PORT=5000
```

```js
require("dotenv").config();
mongoose.connect(process.env.MONGO_URI);
```

### Common Mistakes
- Hardcoding database URLs/secrets instead of using `.env`.
- Forgetting `.env` needs to be in `.gitignore`.
- Running `client` and `server` on the same port — they're separate apps, usually different ports in development.

### Quick Summary
- MERN = MongoDB (data) + Express (API) + React (UI) + Node (runtime).
- `client/` and `server/` are separate projects that talk over HTTP.
- Config/secrets live in `.env`, never in code.

## Where to Go Next

This handbook covers the language and the four MERN pieces. For everything around a real project — git workflows, REST API design conventions, SQL vs NoSQL tradeoffs, Docker, and CI/CD — see `AITS-Docs/` in this workspace instead of duplicating it here.

---
**Previous:** [29-tailwind-css.md](./29-tailwind-css.md) | **Start over:** [01-introduction.md](./01-introduction.md)
