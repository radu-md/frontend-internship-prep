# Interview Prep — JavaScript Questions

Common JavaScript questions for a beginner/intern level.

Read the question, try to answer first, then check the model answer.

---

## What is the difference between `let`, `const`, and `var`?

**Model answer:**
> "`const` declares a variable that cannot be reassigned. `let` declares a variable that can change. Both are block-scoped — they only exist inside the `{}` where they are declared. `var` is the old way — it is function-scoped and can cause bugs, so modern JavaScript uses `let` and `const` instead."

---

## What is the difference between `==` and `===`?

**Model answer:**
> "`===` is strict equality — it checks both value AND type. `==` only checks value and converts types automatically. For example, `'5' == 5` is true but `'5' === 5` is false. Always use `===` in modern JavaScript."

---

## What is an array?

**Model answer:**
> "An array is an ordered list of values. Each value has an index starting at 0. You can loop through it, add items with `push`, filter it, map it, and find items in it."

---

## What is an object?

**Model answer:**
> "An object is a collection of key-value pairs. It groups related data together. For example: `{ name: 'Alex', age: 20 }`. You access values using dot notation: `user.name`."

---

## What is a function?

**Model answer:**
> "A function is a reusable block of code. You define it once and can call it multiple times. It can receive inputs (parameters) and return a result."

---

## What is the difference between a function and an arrow function?

**Model answer:**
> "Arrow functions are a shorter syntax for writing functions. They do not have their own `this` context, which is important in some situations. For most basic uses they behave the same."

---

## What is an event?

**Model answer:**
> "An event is something the user does in the browser — like clicking a button, typing in a field, or submitting a form. You listen for events using `addEventListener`."

---

## What is the DOM?

**Model answer:**
> "The DOM (Document Object Model) is the browser's representation of an HTML page as a tree of objects. JavaScript can read and modify this tree to change what is shown on screen."

---

## What is JSON?

**Model answer:**
> "JSON stands for JavaScript Object Notation. It is a text format used to send and receive data between a frontend and a backend. It looks like a JavaScript object but is always a string when transmitted. You convert it with `JSON.stringify()` and `JSON.parse()`."

---

## What is `async/await`?

**Model answer:**
> "`async/await` is a way to handle asynchronous operations — things that take time, like loading data from an API. `async` marks a function as asynchronous. `await` pauses inside that function until the operation finishes. It makes async code easier to read, similar to regular step-by-step code."

---

## What is `null` vs `undefined`?

**Model answer:**
> "`null` means a value that is intentionally empty. `undefined` means a variable has been declared but no value has been assigned yet."

---

## What does `map()` do?

**Model answer:**
> "`map()` creates a new array by transforming each item. For example, `[1, 2, 3].map(n => n * 2)` returns `[2, 4, 6]`. It does not change the original array."

---

## What does `filter()` do?

**Model answer:**
> "`filter()` creates a new array with only the items that match a condition. For example, `[1, 2, 3, 4].filter(n => n > 2)` returns `[3, 4]`."

---

## What is scope?

**Model answer:**
> "Scope is the area of the code where a variable is accessible. Variables declared with `let` or `const` are block-scoped — they only exist inside the `{}` block where they were created. A variable declared inside a function is not accessible outside that function."

---

## What is `localStorage`?

**Model answer:**
> "`localStorage` is a browser feature that lets you save small amounts of data as key-value pairs. The data stays in the browser even after the page is closed. You use `setItem`, `getItem`, and `removeItem` to manage it."
