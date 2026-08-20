# JS Data Types & Operators — Quick Revision

1. Primitive Data Types

JavaScript has 7 primitive types:
string, number, boolean, undefined, null, bigint, symbol

Examples:
const name = "Neha"; → string
const age = 23; → number
const active = true; → boolean
let x; → undefined
const user = null; → null
const big = 123n; → bigint
const id = Symbol(); → symbol

Objects and arrays are non-primitive/reference types.

2. typeof

Used to check the type of a value.

typeof "hello" → "string"
typeof 23 → "number"
typeof true → "boolean"
typeof undefined → "undefined"

JS quirks:
typeof null → "object"  ← historical JS quirk; null is NOT actually an object
typeof [1, 2, 3] → "object"  ← arrays are a type of object

To specifically check for an array:
Array.isArray([1, 2, 3]) → true

3. Type Conversion

Manually convert one type into another:

Number("23") → 23
String(23) → "23"
Boolean(1) → true
Boolean(0) → false

Number("hello") → NaN

4. Type Coercion

JavaScript sometimes automatically converts types.

"10" + 5 → "105"  → string concatenation
"10" - 5 → 5        → string converted to number

5. Template Literals

Use backticks ` ` and ${} to insert values/expressions into strings.

const name = "Neha";
const message = `Hello ${name}`;

Can also contain expressions:
`Total = ${price * quantity}`

⭐ Remember:

typeof → check type
Number(), String(), Boolean() → manually convert type
Template literals → `Hello ${name}`
Type coercion → JavaScript automatically converts types
null → typeof gives "object" (quirk)
array → typeof gives "object"
Array.isArray() → specifically check if something is an array

You're right. I focused on **data types** and barely covered the **operators** part. For your MERN-focused notes, add this:

6. Operators

Arithmetic operators → used for calculations:

* → addition

- → subtraction

* → multiplication
  / → division
  % → remainder
  ** → exponent/power

Example:
10 + 5 → 15
10 % 3 → 1
2 ** 3 → 8

Assignment operators → assign/update values:
= → assign
+= → add and assign
-= → subtract and assign
*= → multiply and assign
/= → divide and assign

Example:
let x = 10;
x += 5; → x becomes 15

Comparison operators → compare values and return true/false:
=== → equal value AND type
!== → not equal value/type

> → greater than
> < → less than
> = → greater than or equal
> <= → less than or equal

Example:
5 === 5 → true
5 === "5" → false

Logical operators:
&& → AND → true if both conditions are true
|| → OR → true if at least one condition is true
! → NOT → reverses true/false

Example:
age >= 18 && active === true

Increment/decrement:
++ → increase by 1
-- → decrease by 1

Example:
let x = 5;
x++; → 6

⭐ Most important for MERN/React:
===, !==, &&, ||, !, +, -, *, /, %, =, +=

Note: We will study === vs ==, truthy/falsy, and &&/|| short-circuiting separately in more detail because they are important enough to deserve their own topic.

