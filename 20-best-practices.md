# 20. JavaScript Best Practices

**Learning objective:** Learn naming conventions, clean code habits, and common beginner mistakes to avoid.

**Prerequisite:** [19-mini-project-examples.md](./19-mini-project-examples.md)

## Naming Conventions

| Style | Use case | Example |
|---|---|---|
| camelCase | Variables, functions | `firstName`, `getTotal()` |
| PascalCase | Classes | `class UserProfile {}` |
| UPPER_SNAKE_CASE | Constants | `const API_KEY = "..."` |
| kebab-case | File names only | `user-profile.js` |

```js
const firstName = "John";
class UserProfile {}
const API_KEY = "...";
```

## Code Style

- Use meaningful names (`userAge`, not `x`).
- Keep formatting consistent (indentation, spacing).
- Write small, focused functions.
- Avoid magic numbers — use named constants instead.

```js
// Avoid:
if (age > 17) { ... }

// Prefer:
const LEGAL_AGE = 18;
if (age >= LEGAL_AGE) { ... }
```

## Design Principles

- **DRY** (Don't Repeat Yourself): avoid duplicate logic; extract into functions.
- **KISS** (Keep It Simple): prefer the simplest solution that works.
- **Single Responsibility Principle:** each function/class should do one thing.
- **Separation of concerns:** keep structure (HTML), style (CSS), and logic (JS) separate.

## Clean Code Guidelines

- Prefer `const` by default.
- Use `let` only when reassignment is needed.
- Avoid `var` (see [03-variables-and-constants.md](./03-variables-and-constants.md)).
- Return early to avoid deep nesting.
- Keep nesting shallow (avoid many nested `if`s).

```js
// Return early example
function getDiscount(user) {
  if (!user.isMember) return 0;
  return 10;
}
```

## Beginner Mistakes

- Confusing `=` (assignment) with `==`/`===` (comparison) — see [05-operators.md](./05-operators.md).
- Forgetting `return` in functions — see [09-functions.md](./09-functions.md).
- Mutating data accidentally (e.g., modifying an array/object passed into a function).
- Using global variables excessively — see [13-scope.md](./13-scope.md).

### Quick Summary
- Follow consistent naming conventions.
- Apply DRY, KISS, and single responsibility.
- Prefer `const`, shallow nesting, and early returns.

---
**Previous:** [19-mini-project-examples.md](./19-mini-project-examples.md) | **Next:** [21-cheat-sheet.md](./21-cheat-sheet.md)
