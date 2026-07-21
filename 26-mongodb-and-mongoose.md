# 26. MongoDB and Mongoose

**Learning objective:** Store and retrieve data from MongoDB using Mongoose — the "M" in MERN.

**Prerequisite:** [25-express-basics.md](./25-express-basics.md)

## What is MongoDB?

- A NoSQL database — stores flexible JSON-like **documents** in **collections**, instead of rows in tables.

| SQL | MongoDB |
|---|---|
| Table | Collection |
| Row | Document |
| Column | Field |

### Why This Matters: Schema Design

- SQL databases force every row into the same rigid columns (like a strict spreadsheet). MongoDB lets documents in the same collection have slightly different shapes. This flexibility is a genuine **design tradeoff**: faster to start and change, but Mongoose schemas (below) exist specifically to add back some of that structure and safety when you need it.

```js
// A MongoDB document — just JSON
{ _id: "...", name: "Alice", age: 25 }
```

## What is Mongoose?

- An ODM (Object Data Modeling library) for MongoDB — defines a **schema** (shape + types) and gives you a **model** to query with.

## Connecting

```js
const mongoose = require("mongoose");
mongoose.connect("mongodb://localhost:27017/myapp");
```

## Defining a Schema and Model

```js
const userSchema = new mongoose.Schema({
  name: { type: String, required: true },
  age: Number,
  isActive: { type: Boolean, default: true }
});

const User = mongoose.model("User", userSchema);
```

## CRUD with Mongoose

```js
await User.create({ name: "Alice", age: 25 });   // Create
await User.find();                               // Read all
await User.findById(id);                         // Read one
await User.findByIdAndUpdate(id, { age: 26 });   // Update
await User.findByIdAndDelete(id);                // Delete
```

## Wiring It to Express

```js
app.get("/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});
```

### Common Mistakes
- Forgetting `await` on Mongoose calls — you get a Promise, not the data.
- Skipping schema validation (`required`, `type`) — bad data slips in silently.
- Calling `mongoose.connect()` more than once per app.

### Quick Summary
- MongoDB stores documents in collections (no fixed table structure).
- Mongoose adds schemas/models on top for structure and validation.
- Every Mongoose query is a Promise — always `await` it.

---
**Previous:** [25-express-basics.md](./25-express-basics.md) | **Next:** [27-react-basics.md](./27-react-basics.md)
