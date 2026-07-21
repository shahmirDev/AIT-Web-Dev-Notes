# 1. Introduction to JavaScript

**Learning objective:** Understand what JavaScript is, where it runs, and how it fits with HTML/CSS.

## What is JavaScript?

- A lightweight, interpreted programming language.
- Adds **interactivity** and **logic** to web pages.
- Can run on the browser (client-side) and on servers (via Node.js).

## How the Web Actually Works (Client-Server Model)

- Think of a restaurant: you (the **client/browser**) sit at a table and ask a waiter for food. The waiter takes your order to the **kitchen (server)**, which prepares it and sends it back.
- On the web: your browser sends a **request** (e.g. "give me this webpage"), a server processes it and sends back a **response** (HTML, data, etc.).
- This request-response pattern is the foundation almost everything else in this handbook builds on — we'll revisit this exact analogy when we get to servers and full-stack apps later.

## Where JavaScript Runs

| Environment | Example |
|---|---|
| Browser | Chrome, Firefox, Edge (via built-in JS engine) |
| Server | Node.js |
| Mobile/Desktop apps | React Native, Electron |

## JavaScript's Role with HTML & CSS

- **HTML** → structure (content)
- **CSS** → style (appearance)
- **JavaScript** → behavior (interactivity/logic)

```html
<button onclick="alert('Hello!')">Click me</button>
```

### Quick Summary
- JS makes web pages interactive.
- Runs in browsers and on servers (Node.js).
- Works alongside HTML (structure) and CSS (style).

---
**Next:** [02-javascript-syntax.md](./02-javascript-syntax.md)
