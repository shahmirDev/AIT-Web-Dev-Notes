# 29. Tailwind CSS

**Learning objective:** Style React components using Tailwind's utility classes instead of writing custom CSS files.

**Prerequisite:** [28-react-hooks-and-state.md](./28-react-hooks-and-state.md)

## What is Tailwind?

- A utility-first CSS framework — style elements with small, single-purpose classes directly in your markup, instead of writing separate CSS files.

```jsx
// Custom CSS way
<button className="btn-primary">Save</button>

// Tailwind way
<button className="bg-blue-500 text-white px-4 py-2 rounded">Save</button>
```

## Common Utility Categories

| Category | Examples | Meaning |
|---|---|---|
| Spacing | `p-4`, `m-2`, `px-6` | padding/margin (4 = 1rem) |
| Layout | `flex`, `grid`, `justify-center`, `items-center` | flexbox/grid layout |
| Sizing | `w-full`, `h-screen` | width/height |
| Color | `bg-blue-500`, `text-white` | background/text color |
| Typography | `text-lg`, `font-bold` | font size/weight |
| Responsive | `sm:`, `md:`, `lg:` prefixes | apply a class only above a screen size |

## Example: A Card Component

```jsx
function Card({ title, text }) {
  return (
    <div className="max-w-sm mx-auto p-6 rounded-lg shadow-md bg-white">
      <h2 className="text-xl font-bold mb-2">{title}</h2>
      <p className="text-gray-600">{text}</p>
    </div>
  );
}
```

## Responsive Example

```jsx
<div className="text-sm md:text-lg lg:text-2xl">
  Grows on bigger screens
</div>
```

### Common Mistakes
- Mixing Tailwind with lots of custom CSS — pick one approach for a component, don't fight the utility classes.
- Forgetting responsive prefixes apply "this size and up," not "only this size."
- Not configuring Tailwind to scan your component files — unused classes get removed in production if the config doesn't see them.

### Quick Summary
- Utility classes replace hand-written CSS — style directly in JSX.
- Spacing/layout/color/typography classes cover most needs.
- Responsive prefixes (`sm:`, `md:`, `lg:`) apply a style from that breakpoint upward.

---
**Previous:** [28-react-hooks-and-state.md](./28-react-hooks-and-state.md) | **Next:** [30-mern-project-structure.md](./30-mern-project-structure.md)
