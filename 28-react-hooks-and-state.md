# 28. React Hooks and State

**Learning objective:** Make components interactive with `useState`, and handle side effects (like API calls) with `useEffect`.

**Prerequisite:** [27-react-basics.md](./27-react-basics.md)

## useState

- Adds state to a function component. Calling the setter re-renders the component.

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Clicked {count} times
    </button>
  );
}
```

- Never mutate state directly (`count++`) — always use the setter.

### Why This Matters: Unidirectional Data Flow

- React apps follow a one-way street: data (state) flows *down* from parent to child via props, and events flow *up* (a child tells its parent something happened, e.g. a click), which then updates state and flows back down. This "state management" discipline is why React apps stay predictable even as they grow — data doesn't randomly change from unexpected places.
- Like water flowing downhill: it only goes one direction, which makes it easy to trace where a value came from.

## useEffect

- Runs code after render — for things outside React's normal flow (API calls, timers, subscriptions).

```jsx
import { useEffect, useState } from "react";

function Clock() {
  const [time, setTime] = useState(new Date());

  useEffect(() => {
    const id = setInterval(() => setTime(new Date()), 1000);
    return () => clearInterval(id); // cleanup, runs before next effect / on unmount
  }, []); // empty array = run once, on mount

  return <p>{time.toLocaleTimeString()}</p>;
}
```

- The dependency array (`[]`) controls when the effect re-runs: empty = once, `[value]` = whenever `value` changes, omitted = every render.

## Fetching Data (combining async JS + hooks)

```jsx
function Users() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    async function load() {
      const res = await fetch("/api/users");
      const data = await res.json();
      setUsers(data);
    }
    load();
  }, []);

  return (
    <ul>
      {users.map(u => <li key={u.id}>{u.name}</li>)}
    </ul>
  );
}
```

### Common Mistakes
- Missing/wrong dependency array — causes infinite loops or stale data.
- Mutating state directly instead of calling the setter.
- Forgetting the cleanup function for timers/subscriptions (memory leaks).
- Making `useEffect`'s callback itself `async` — wrap the async code in an inner function instead (as above).

### Quick Summary
- `useState` → component state, re-renders on change.
- `useEffect` → side effects, controlled by the dependency array.
- Fetch inside `useEffect` with an inner `async` function, store the result with `useState`.

---
**Previous:** [27-react-basics.md](./27-react-basics.md) | **Next:** [29-tailwind-css.md](./29-tailwind-css.md)
