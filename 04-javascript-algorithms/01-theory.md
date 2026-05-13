# Module 04 — Theory: JavaScript Algorithms and Common Patterns

## What are algorithms?

An algorithm is a set of steps to solve a problem.

In JavaScript, you will use algorithms every day — not just in interviews.
Sorting a list, searching for an item, grouping data, removing duplicates — these are all common tasks that require knowing the right pattern.

This module is about **practical patterns** you will use in real projects.

---

## Sorting

JavaScript arrays have a built-in `.sort()` method.

### Default sort (alphabetical)

```js
const fruits = ['banana', 'apple', 'cherry'];
fruits.sort();
console.log(fruits); // ['apple', 'banana', 'cherry']
```

**Warning:** The default sort converts items to strings first. This causes problems with numbers:

```js
const numbers = [10, 2, 30, 5];
numbers.sort();
console.log(numbers); // [10, 2, 30, 5] ← WRONG
```

### Sort numbers correctly

Use a **compare function**:

```js
const numbers = [10, 2, 30, 5];

// Ascending (smallest first)
numbers.sort((a, b) => a - b);
console.log(numbers); // [2, 5, 10, 30]

// Descending (largest first)
numbers.sort((a, b) => b - a);
console.log(numbers); // [30, 10, 5, 2]
```

### Sort objects by a property

```js
const products = [
  { name: 'Tablet', price: 349 },
  { name: 'Phone', price: 699 },
  { name: 'Laptop', price: 999 }
];

// Sort by price ascending
products.sort((a, b) => a.price - b.price);

// Sort by name alphabetically
products.sort((a, b) => a.name.localeCompare(b.name));
```

`.sort()` modifies the original array. To sort without changing the original:

```js
const sorted = [...products].sort((a, b) => a.price - b.price);
```

---

## Searching

### Linear search (find by value)

```js
const users = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' },
  { id: 3, name: 'Charlie' }
];

// Find the first match
const user = users.find(u => u.id === 2);
console.log(user); // { id: 2, name: 'Bob' }

// Find the index
const index = users.findIndex(u => u.id === 2);
console.log(index); // 1

// Check if any match exists
const exists = users.some(u => u.name === 'Bob');
console.log(exists); // true

// Check if ALL match a condition
const allAdults = users.every(u => u.id > 0);
console.log(allAdults); // true
```

### Search in strings

```js
const text = 'Hello Angular world';

text.includes('Angular');     // true
text.startsWith('Hello');     // true
text.endsWith('world');       // true
text.indexOf('Angular');      // 6 (position)
```

---

## Deduplication (removing duplicates)

```js
const tags = ['css', 'html', 'css', 'js', 'html'];

// Using Set
const unique = [...new Set(tags)];
console.log(unique); // ['css', 'html', 'js']
```

For arrays of objects, use `filter`:

```js
const items = [
  { id: 1, name: 'A' },
  { id: 2, name: 'B' },
  { id: 1, name: 'A' }
];

const unique = items.filter(
  (item, index, arr) => arr.findIndex(i => i.id === item.id) === index
);
```

---

## Grouping

Group an array of objects by a property value:

```js
const products = [
  { name: 'Laptop', category: 'electronics' },
  { name: 'T-Shirt', category: 'clothing' },
  { name: 'Phone', category: 'electronics' },
  { name: 'Jeans', category: 'clothing' }
];

const grouped = products.reduce((acc, product) => {
  const key = product.category;
  if (!acc[key]) acc[key] = [];
  acc[key].push(product);
  return acc;
}, {});

console.log(grouped);
// {
//   electronics: [{ name: 'Laptop', ... }, { name: 'Phone', ... }],
//   clothing: [{ name: 'T-Shirt', ... }, { name: 'Jeans', ... }]
// }
```

---

## Transformation with `reduce`

`reduce` is the most powerful array method. It processes an array and produces a single result.

```js
// Sum
const total = [10, 20, 30].reduce((sum, n) => sum + n, 0); // 60

// Count occurrences
const words = ['apple', 'banana', 'apple', 'cherry', 'banana', 'apple'];
const count = words.reduce((acc, word) => {
  acc[word] = (acc[word] || 0) + 1;
  return acc;
}, {});
// { apple: 3, banana: 2, cherry: 1 }

// Flatten one level
const nested = [[1, 2], [3, 4], [5]];
const flat = nested.reduce((acc, arr) => [...acc, ...arr], []);
// [1, 2, 3, 4, 5]

// Or use the built-in:
const flat2 = nested.flat(); // same result
```

---

## Chaining array methods

You can chain multiple methods together:

```js
const products = [
  { name: 'Laptop', price: 999, category: 'electronics' },
  { name: 'T-Shirt', price: 25, category: 'clothing' },
  { name: 'Phone', price: 699, category: 'electronics' },
  { name: 'Tablet', price: 349, category: 'electronics' }
];

// Get names of electronics under $800, sorted by price
const result = products
  .filter(p => p.category === 'electronics')
  .filter(p => p.price < 800)
  .sort((a, b) => a.price - b.price)
  .map(p => p.name);

console.log(result); // ['Tablet', 'Phone']
```

---

## Common string patterns

```js
const text = '  Hello, World!  ';

text.trim();                    // 'Hello, World!'
text.toLowerCase();             // '  hello, world!  '
text.toUpperCase();             // '  HELLO, WORLD!  '
text.replace('World', 'JS');    // '  Hello, JS!  '
text.split(', ');               // ['  Hello', 'World!  ']
'Hello'.split('').reverse().join(''); // 'olleH'

// Template literals
const name = 'Alex';
const greeting = `Hello, ${name}!`; // 'Hello, Alex!'
```

---

## Summary

| Pattern | Method(s) | Use for |
|---|---|---|
| Sort alphabetically | `.sort()` | Strings |
| Sort numerically | `.sort((a, b) => a - b)` | Numbers |
| Sort objects | `.sort((a, b) => a.prop - b.prop)` | Objects by property |
| Find one item | `.find()` | First match |
| Find position | `.findIndex()` | Index of match |
| Check existence | `.includes()`, `.some()` | Does it exist? |
| Remove duplicates | `[...new Set(arr)]` | Unique values |
| Group by property | `.reduce()` | Group into object |
| Sum / accumulate | `.reduce()` | Single result from array |
| Chain transforms | `.filter().map().sort()` | Complex data processing |

**Next step:** Read `02-terminology.md`.
