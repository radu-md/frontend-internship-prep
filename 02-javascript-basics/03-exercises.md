# Module 02 — Exercises: JavaScript Basics

Write your code in a `.js` file or directly in the browser console.

Read each goal carefully before writing anything.
Try to solve it without looking at the theory first.

---

## Exercise 1 — Variables and types

**Goal:** Declare variables for a user profile and print them.

1. Create a `const` for a name (string)
2. Create a `let` for an age (number)
3. Create a `const` for `isLoggedIn` (boolean, set to `false`)
4. Print all three with `console.log()`
5. Change `age` to a new value and print it again

---

## Exercise 2 — Arrays

**Goal:** Work with an array of products.

```js
const products = ['laptop', 'phone', 'tablet', 'monitor', 'keyboard'];
```

1. Print the first item
2. Print the last item (use `.length - 1`)
3. Print the total number of items
4. Use `filter` to create a new array with only items longer than 6 characters
5. Use `map` to create a new array where every name is UPPERCASE (hint: `.toUpperCase()`)
6. Use `find` to get the first item that starts with the letter 'p'

---

## Exercise 3 — Objects

**Goal:** Create a user object and work with it.

1. Create an object called `user` with these properties:
   - `name` (string)
   - `age` (number)
   - `email` (string)
   - `isAdmin` (boolean, set to `false`)

2. Print the user's name using dot notation
3. Print the user's email using bracket notation (`user['email']`)
4. Change `isAdmin` to `true`
5. Add a new property `city` with any value
6. Print the full object with `console.log(user)`

---

## Exercise 4 — Functions

**Goal:** Write small functions.

1. Write a function `greet(name)` that returns `"Hello, [name]!"`
   - Call it with your name and print the result

2. Write a function `add(a, b)` that returns the sum of two numbers
   - Call it with `3` and `7`, print the result

3. Write an arrow function `isAdult(age)` that returns `true` if age is 18 or more, `false` otherwise
   - Test it with ages 15 and 21

4. Write a function `getFullName(firstName, lastName)` that returns the full name as one string
   - Call it and print the result

---

## Exercise 5 — Loops

**Goal:** Use loops to process data.

```js
const scores = [85, 42, 91, 67, 73, 55, 88];
```

1. Use a `for...of` loop to print every score
2. Use a `for` loop to print the index and score together:
   - Example output: `Score 0: 85`
3. Use `filter` to get only scores above 70
4. Use `map` to multiply every score by 2

---

## Exercise 6 — Conditions

**Goal:** Write functions that use conditions.

1. Write a function `grade(score)` that returns:
   - `'A'` if score >= 90
   - `'B'` if score >= 75
   - `'C'` if score >= 60
   - `'F'` otherwise

2. Test it with scores: 95, 80, 65, 40

3. Write a function `isEven(n)` that returns `true` if `n` is even, `false` if odd
   - Test it with 4 and 7

---

## Exercise 7 — Combine it all

**Goal:** Build a simple product filter function.

```js
const products = [
  { name: 'Laptop', price: 999, category: 'electronics' },
  { name: 'T-Shirt', price: 25, category: 'clothing' },
  { name: 'Phone', price: 699, category: 'electronics' },
  { name: 'Jeans', price: 59, category: 'clothing' },
  { name: 'Headphones', price: 149, category: 'electronics' }
];
```

1. Use `filter` to get only `electronics` products
2. Use `filter` to get products with price under 200
3. Use `map` to create a new array with only the product names
4. Use `find` to get the product named `'Phone'`
5. Print results of each step

---

**Next step:** Go to `04-mini-challenge.md`.
