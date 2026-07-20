# 23. npm and Modules

**Learning objective:** Learn how JS code is split across files (modules) and how npm manages a project's dependencies — the setup every Node/Express/React project starts with.

**Prerequisite:** [22-async-javascript.md](./22-async-javascript.md)

## Why Modules?

- Split code into separate files instead of one giant file.
- Each file only exposes what it explicitly exports.

## CommonJS (Node's original system)

```js
// math.js
function add(a, b) { return a + b; }
module.exports = { add };

// app.js
const { add } = require("./math");
add(2, 3); // 5
```

## ES Modules (modern standard, used in React)

```js
// math.js
export function add(a, b) { return a + b; }

// app.js
import { add } from "./math.js";
add(2, 3); // 5
```

- Node uses ES Modules when `package.json` has `"type": "module"`, otherwise it assumes CommonJS.

## npm Basics

| Command | Purpose |
|---|---|
| `npm init -y` | Create a `package.json` with defaults |
| `npm install <package>` | Add a dependency |
| `npm install -D <package>` | Add a dev-only dependency (e.g. testing tools) |
| `npm install` | Install everything listed in `package.json` |
| `npm run <script>` | Run a custom script |

## package.json

```json
{
  "name": "my-app",
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  },
  "dependencies": { "express": "^4.19.0" },
  "devDependencies": { "nodemon": "^3.0.0" }
}
```

- `dependencies` → needed to run the app.
- `devDependencies` → only needed while developing (linters, test runners).
- `node_modules/` is never committed to git — it's rebuilt from `package.json` with `npm install`.

### Common Mistakes
- Mixing `require` and `import` in the same file without matching config — pick one system per project.
- Committing `node_modules/` to git (add it to `.gitignore` instead).
- Forgetting `^` in a version number means "compatible upgrades allowed," not an exact pin.

### Quick Summary
- CommonJS: `require`/`module.exports` (older, still common in Node).
- ES Modules: `import`/`export` (modern, used in React/Vite projects).
- `package.json` tracks dependencies and scripts; `node_modules/` is never committed.

---
**Previous:** [22-async-javascript.md](./22-async-javascript.md) | **Next:** [24-nodejs-basics.md](./24-nodejs-basics.md)
