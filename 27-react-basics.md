# 27. React Basics

**Learning objective:** Build a UI from components using JSX and props — the "R" in MERN.

**Prerequisite:** [26-mongodb-and-mongoose.md](./26-mongodb-and-mongoose.md)

## What is React?

- A library for building UIs out of reusable **components**.
- You describe what the UI should look like for a given state; React updates the page for you.

### Why This Matters: Component-Based Architecture

- Instead of building one giant page, React encourages breaking the UI into small, reusable pieces — like Lego blocks. A `Card`, a `Button`, a `UserList` — each is self-contained and can be reused or swapped without touching the rest of the app.
- This is the frontend equivalent of the layered thinking from Express: instead of routes/middleware/models, it's components that compose together to build the full page.

## JSX

- Looks like HTML, but it's JavaScript. Must return a **single** root element.

```jsx
function Welcome() {
  return <h1>Hello, world!</h1>;
}
```

```jsx
// Embedding JS values with {}
function Greeting() {
  const name = "Alice";
  return <h1>Hello, {name}!</h1>;
}
```

## Function Components

```jsx
function Card() {
  return (
    <div>
      <h2>Title</h2>
      <p>Some text</p>
    </div>
  );
}

export default Card;
```

## Props

- How a parent passes data down to a child component. Read-only — never modified by the child.

```jsx
function Greeting({ name }) {
  return <p>Hello, {name}</p>;
}

// usage
<Greeting name="Alice" />
```

## Rendering Lists

- Use `.map()` (see [10-arrays.md](./10-arrays.md)) to turn an array into elements. Each item needs a unique `key`.

```jsx
const users = [{ id: 1, name: "Alice" }, { id: 2, name: "Bob" }];

function UserList() {
  return (
    <ul>
      {users.map(user => <li key={user.id}>{user.name}</li>)}
    </ul>
  );
}
```

### Common Mistakes
- Forgetting the `key` prop when rendering a list — React warns and re-renders inefficiently.
- Returning multiple root elements from JSX without wrapping them (use `<> </>` — a fragment).
- Trying to modify `props` directly — treat them as read-only.

### Quick Summary
- Components are functions that return JSX.
- Props pass data from parent to child, read-only.
- `.map()` + `key` renders lists of components.

---
**Previous:** [26-mongodb-and-mongoose.md](./26-mongodb-and-mongoose.md) | **Next:** [28-react-hooks-and-state.md](./28-react-hooks-and-state.md)
