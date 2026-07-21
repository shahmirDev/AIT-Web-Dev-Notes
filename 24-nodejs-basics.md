# 24. Node.js Basics

**Learning objective:** Understand what Node.js is and use it to run JS outside the browser — the "N" in MERN.

**Prerequisite:** [23-npm-and-modules.md](./23-npm-and-modules.md)

## What is Node.js?

- A runtime that lets JS run outside the browser (on a server, your machine, anywhere).
- Built on Chrome's V8 engine. No `window` or `document` — instead it has file system, network, and OS access.

### Why This Matters: Language vs. Runtime

- JavaScript (the *language* — syntax, logic, rules) and Node.js (a *runtime* — the environment that actually executes it and gives it powers like reading files) are different things. The browser is another runtime for the same language, just with different powers (DOM, no file access).
- Same recipe (JS), different kitchens (browser vs. Node) — each kitchen has different appliances available.

## Running a File

```bash
node app.js
```

## Core Modules

| Module | Purpose | Example |
|---|---|---|
| `fs` | Read/write files | `fs.readFileSync("data.txt", "utf8")` |
| `path` | Work with file paths safely | `path.join(__dirname, "data.txt")` |
| `os` | Info about the machine | `os.platform()` |

```js
const fs = require("fs");

const data = fs.readFileSync("notes.txt", "utf8");
console.log(data);
```

## A Basic Server (before Express)

```js
const http = require("http");

const server = http.createServer((req, res) => {
  res.writeHead(200, { "Content-Type": "text/plain" });
  res.end("Hello from Node!");
});

server.listen(3000, () => console.log("Server running on port 3000"));
```

- This is what Express simplifies — routing, JSON handling, and middleware by hand get tedious fast (see next file).

### Common Mistakes
- Using `fs.readFileSync` (blocking) for large files in a server — prefer `fs.promises.readFile` with `await`.
- Forgetting Node has no `window`/`document`/`alert` — those are browser-only.
- Not calling `server.listen()` — the server won't actually start.

### Quick Summary
- Node.js = JS runtime for servers/scripts, no browser APIs.
- `fs`/`path`/`os` are built-in modules for file and system access.
- `http.createServer` builds a raw server — Express (next) makes this easier.

---
**Previous:** [23-npm-and-modules.md](./23-npm-and-modules.md) | **Next:** [25-express-basics.md](./25-express-basics.md)
