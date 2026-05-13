# Module 02 — Terminology: JavaScript Basics

Learn these words. Try to explain each one without reading after you finish.

---

## Variables and types

**Variable**
A named storage for a value.
Example: `let score = 10;` — the variable `score` holds the value `10`.

**`let`**
Declares a variable whose value can change.
Example: `let count = 0; count = 1;`

**`const`**
Declares a variable whose value cannot be reassigned.
Example: `const name = 'Alex';`

**String**
A text value, written in quotes.
Example: `'hello'`, `"world"`

**Number**
A numeric value.
Example: `42`, `3.14`

**Boolean**
A value that is either `true` or `false`.
Example: `let isLoggedIn = false;`

**`null`**
An intentionally empty value — means "nothing here on purpose".

**`undefined`**
A variable that has been declared but not given a value yet.

---

## Arrays

**Array**
An ordered list of values.
Example: `['apple', 'banana', 'cherry']`

**Index**
The position of an item in an array. Starts at `0`.
Example: `fruits[0]` gives the first item.

**`length`**
The number of items in an array.
Example: `['a', 'b', 'c'].length` is `3`.

**`map()`**
Creates a new array by transforming each item.
Example: `[1, 2, 3].map(n => n * 2)` → `[2, 4, 6]`

**`filter()`**
Creates a new array with only items that pass a condition.
Example: `[1, 2, 3].filter(n => n > 1)` → `[2, 3]`

**`find()`**
Returns the first item that matches a condition.
Example: `[1, 2, 3].find(n => n > 1)` → `2`

**`push()`**
Adds an item to the end of an array.
Example: `arr.push('new item')`

---

## Objects

**Object**
A collection of key-value pairs.
Example: `{ name: 'Alex', age: 20 }`

**Key (property)**
The name used to access a value in an object.
Example: in `{ name: 'Alex' }`, the key is `name`.

**Value**
The data stored under a key.
Example: in `{ name: 'Alex' }`, the value is `'Alex'`.

**Dot notation**
Accessing an object value using a dot.
Example: `user.name`

---

## Functions

**Function**
A block of code that does something. You can call it whenever you need it.
Example: `function sayHi() { console.log('Hi'); }`

**Parameter**
The variable defined in a function that receives input.
Example: in `function greet(name)`, `name` is the parameter.

**Argument**
The actual value passed when calling a function.
Example: `greet('Alex')` — `'Alex'` is the argument.

**`return`**
Sends a value back from a function.
Example: `function add(a, b) { return a + b; }`

**Arrow function**
A shorter way to write a function.
Example: `const add = (a, b) => a + b;`

---

## Conditions and loops

**Condition**
A check that results in `true` or `false`.
Example: `age >= 18`

**`if / else`**
Runs different code depending on a condition.

**`===`**
Strict equality — checks both value and type. Always use this over `==`.
Example: `'5' === 5` is `false` because one is a string and one is a number.

**Loop**
Repeats a block of code.
Example: `for`, `for...of`

---

## Other

**`console.log()`**
Prints a value to the browser console. Used for debugging.

**JSON**
JavaScript Object Notation. A text format for data — used for sending data between frontend and backend.

**Module**
A separate JavaScript file. You can `export` things from it and `import` them elsewhere.

**`import` / `export`**
Keywords used to share code between modules (files).

---

**Next step:** Go to `03-exercises.md` to practice.
