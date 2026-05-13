# Module 02 — Theory: JavaScript Basics

## What is JavaScript?

JavaScript is a programming language that runs in the browser.

While HTML gives structure and CSS gives appearance, **JavaScript makes the page interactive**.

Examples of what JavaScript does:
- Show or hide content when a button is clicked
- Validate a form before submitting
- Load data from a server and display it on the page
- Build a to-do list where you can add and remove items

---

## Variables

A variable stores a value so you can use it later.

```js
let name = 'Alex';
const age = 20;
```

| Keyword | Can change? | Use for |
|---|---|---|
| `let` | Yes | Values that will change |
| `const` | No | Values that will not change |
| `var` | Yes | Old style — avoid in modern code |

---

## Data types

JavaScript has several basic types of values:

```js
let text = 'Hello';         // string
let number = 42;            // number
let isReady = true;         // boolean
let nothing = null;         // null (empty on purpose)
let unknown;                // undefined (no value set yet)
```

---

## Arrays

An array is a list of values.

```js
let fruits = ['apple', 'banana', 'cherry'];

console.log(fruits[0]);  // 'apple'  (index starts at 0)
console.log(fruits.length);  // 3
```

### Useful array methods

```js
let numbers = [3, 1, 4, 1, 5];

// map — transform each item, returns a new array
let doubled = numbers.map(n => n * 2);  // [6, 2, 8, 2, 10]

// filter — keep only items that match a condition
let bigNumbers = numbers.filter(n => n > 2);  // [3, 4, 5]

// find — returns the first item that matches
let found = numbers.find(n => n > 3);  // 4

// includes — check if a value exists
let hasOne = numbers.includes(1);  // true

// push — add to end
numbers.push(9);  // [3, 1, 4, 1, 5, 9]
```

---

## Objects

An object groups related values together using keys.

```js
let user = {
  name: 'Alex',
  age: 20,
  isLoggedIn: false
};

console.log(user.name);    // 'Alex'
console.log(user['age']);  // 20  (alternative syntax)

user.isLoggedIn = true;    // update a value
```

---

## Functions

A function is a block of code you can run whenever you call it.

```js
function greet(name) {
  return 'Hello, ' + name + '!';
}

console.log(greet('Alex'));  // 'Hello, Alex!'
```

### Arrow functions (shorter syntax)

```js
const greet = (name) => {
  return 'Hello, ' + name + '!';
};

// Even shorter for single-line returns:
const greet = name => 'Hello, ' + name + '!';
```

---

## Conditions

```js
let age = 20;

if (age >= 18) {
  console.log('Adult');
} else {
  console.log('Minor');
}
```

### Comparison operators

| Operator | Meaning |
|---|---|
| `===` | Strictly equal (value AND type) |
| `!==` | Not equal |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal |
| `<=` | Less than or equal |

Always use `===` instead of `==` in modern JavaScript.

---

## Loops

### `for` loop

```js
for (let i = 0; i < 3; i++) {
  console.log(i);  // 0, 1, 2
}
```

### `for...of` loop (for arrays)

```js
let fruits = ['apple', 'banana', 'cherry'];

for (let fruit of fruits) {
  console.log(fruit);  // apple, banana, cherry
}
```

---

## JSON

JSON (JavaScript Object Notation) is a format for storing and sending data.

It looks like a JavaScript object, but it is always a string when sent over the internet.

```json
{
  "name": "Alex",
  "age": 20,
  "skills": ["HTML", "CSS", "JavaScript"]
}
```

Convert between JSON and JavaScript:

```js
// Object to JSON string
const json = JSON.stringify({ name: 'Alex' });

// JSON string to object
const obj = JSON.parse('{"name":"Alex"}');
```

---

## ES Modules (basics)

Modules let you split code into separate files and import what you need.

```js
// math.js
export function add(a, b) {
  return a + b;
}

// main.js
import { add } from './math.js';
console.log(add(2, 3));  // 5
```

---

## Summary

| Concept | Key point |
|---|---|
| `let` / `const` | Store values; prefer `const`, use `let` when value changes |
| Data types | string, number, boolean, null, undefined |
| Array | Ordered list; use `map`, `filter`, `find` |
| Object | Key-value pairs for grouping data |
| Function | Reusable block of code |
| `===` | Always use instead of `==` |
| Loop | `for` or `for...of` to repeat code |
| JSON | Format for sending/receiving data |

**Next step:** Read `02-terminology.md` to review key words.
