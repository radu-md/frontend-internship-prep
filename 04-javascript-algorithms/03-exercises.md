# Module 04 — Exercises: JavaScript Algorithms and Common Patterns

Use the browser console or a `.js` file to write and test each solution.

---

## Exercise 1 — Sorting numbers

```js
const scores = [42, 87, 15, 93, 61, 28, 74];
```

1. Sort ascending (smallest first)
2. Sort descending (largest first)
3. Print both results — make sure the original array is not changed

---

## Exercise 2 — Sorting objects

```js
const students = [
  { name: 'Charlie', grade: 78 },
  { name: 'Alice', grade: 92 },
  { name: 'Bob', grade: 85 },
  { name: 'Diana', grade: 67 }
];
```

1. Sort by `grade` ascending
2. Sort by `grade` descending
3. Sort by `name` alphabetically (use `.localeCompare()`)
4. Print each sorted array

---

## Exercise 3 — Searching

```js
const products = [
  { id: 1, name: 'Laptop', price: 999, inStock: true },
  { id: 2, name: 'Phone', price: 699, inStock: false },
  { id: 3, name: 'Tablet', price: 349, inStock: true },
  { id: 4, name: 'Monitor', price: 249, inStock: true }
];
```

1. Find the product with `id === 3`
2. Find the index of the product named `'Phone'`
3. Check if any product is out of stock (`.some()`)
4. Check if all products have a price above 100 (`.every()`)
5. Check if the array includes a product with `id === 99` (use `.some()`)

---

## Exercise 4 — Deduplication

1. Remove duplicates from this array:
   ```js
   const tags = ['angular', 'css', 'html', 'angular', 'js', 'css', 'angular'];
   ```

2. Remove duplicate users by `id`:
   ```js
   const users = [
     { id: 1, name: 'Alice' },
     { id: 2, name: 'Bob' },
     { id: 1, name: 'Alice' },
     { id: 3, name: 'Charlie' }
   ];
   ```

---

## Exercise 5 — Grouping

```js
const tasks = [
  { title: 'Fix login bug', status: 'done' },
  { title: 'Add dark mode', status: 'pending' },
  { title: 'Write tests', status: 'pending' },
  { title: 'Deploy to staging', status: 'done' },
  { title: 'Update docs', status: 'in-progress' }
];
```

Use `reduce` to group tasks by `status`.

Expected result shape:
```js
{
  done: [...],
  pending: [...],
  'in-progress': [...]
}
```

---

## Exercise 6 — reduce practice

```js
const orders = [
  { product: 'Laptop', quantity: 1, price: 999 },
  { product: 'Mouse', quantity: 2, price: 29 },
  { product: 'Keyboard', quantity: 1, price: 79 },
  { product: 'Monitor', quantity: 2, price: 249 }
];
```

1. Calculate the total cost of all orders (quantity × price for each, then sum)
2. Count how many individual items were ordered in total (sum of all quantities)
3. Find the most expensive single item (highest `price`)

---

## Exercise 7 — Chaining

```js
const employees = [
  { name: 'Alice', department: 'engineering', salary: 4500 },
  { name: 'Bob', department: 'marketing', salary: 3200 },
  { name: 'Charlie', department: 'engineering', salary: 5100 },
  { name: 'Diana', department: 'engineering', salary: 4800 },
  { name: 'Eve', department: 'marketing', salary: 3800 }
];
```

Using method chaining (one expression):
1. Get the names of engineering employees with salary > 4600, sorted alphabetically
2. Get the total salary of all marketing employees
3. Get the top 2 highest-paid employees (any department) — return their names and salaries

---

## Exercise 8 — String patterns

```js
const sentence = '  the quick brown fox jumps over the lazy dog  ';
```

1. Trim whitespace from both ends
2. Capitalize the first letter of the sentence
3. Count how many words it contains
4. Find the longest word
5. Reverse the entire sentence word by word (words in reverse order, words themselves not reversed)

Expected for step 5:
```
'dog lazy the over jumps fox brown quick the'
```

---

**Next step:** Go to `04-mini-challenge.md`.
