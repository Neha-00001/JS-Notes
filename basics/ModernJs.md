# Modern JS — Quick Revision

1. Optional Chaining `?.`

Used to safely access nested properties that may not exist.

user?.address?.city

If a property is missing → returns `undefined` instead of throwing an error.

`?.` → "If it exists, continue; otherwise return undefined."

2. Nullish Coalescing `??`

Used to provide a fallback when a value is `null` or `undefined`.

const name = null;
const result = name ?? "Guest";  // "Guest"

`??` → fallback only for `null` / `undefined`.

Difference:
`??` → null/undefined only
`||` → any falsy value (`0`, `""`, `false`, `null`, `undefined`, `NaN`)

3. Object Methods

Object.keys(obj) → returns array of keys

Object.values(obj) → returns array of values

Object.entries(obj) → returns array of `[key, value]` pairs

Example:
const user = { name: "Neha", age: 23 };

Object.keys(user) → ["name", "age"]
Object.values(user) → ["Neha", 23]
Object.entries(user) → [["name", "Neha"], ["age", 23]]

4. Computed Properties

Used when the property name is stored in a variable.

const key = "name";

const user = {
[key]: "Neha"
};

Result → `{ name: "Neha" }`

`[variable]` → use the variable's value as the property name.

⭐ Remember:

`?.` → safely access
`??` → fallback for null/undefined
`Object.keys()` → keys
`Object.values()` → values
`Object.entries()` → key + value
`[variable]` → dynamic property name
