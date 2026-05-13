# Module 04 — Terminology: JavaScript Algorithms and Common Patterns

---

**Algorithm**
A step-by-step process to solve a problem.
Example: to find the largest number in a list, check each number one by one and keep track of the biggest seen so far.

**Sorting**
Arranging items in a specific order — alphabetical, numeric ascending, numeric descending.
Example: `[3, 1, 2].sort((a, b) => a - b)` → `[1, 2, 3]`

**Compare function**
A function passed to `.sort()` that tells JavaScript how to compare two items.
- Returns negative → `a` comes first
- Returns positive → `b` comes first
- Returns 0 → order does not change
Example: `(a, b) => a - b` sorts numbers ascending.

**Searching**
Looking through data to find a specific item or check if it exists.

**Linear search**
Checking items one by one from the start until a match is found.
Example: `.find()` performs a linear search.

**`.find()`**
Returns the first item in an array that matches a condition.
Example: `users.find(u => u.id === 2)`

**`.findIndex()`**
Returns the index (position) of the first matching item. Returns `-1` if not found.

**`.some()`**
Returns `true` if at least one item matches a condition.

**`.every()`**
Returns `true` if ALL items match a condition.

**Deduplication**
Removing duplicate values from an array.
Example: `[...new Set([1, 1, 2, 3])]` → `[1, 2, 3]`

**`Set`**
A built-in JavaScript collection that only stores unique values. Duplicates are automatically ignored.

**Grouping**
Organizing items into groups based on a shared property.
Example: grouping products by category into an object.

**`reduce()`**
An array method that processes all items and produces a single result — a number, string, object, or array.
It is the most flexible array method.

**Accumulator**
The variable in `reduce()` that collects the result as it processes each item.
Example: `(acc, item) => { ... }` — `acc` is the accumulator.

**Chaining**
Calling multiple array methods one after another on the same array.
Example: `.filter().map().sort()`

**Immutability**
Not changing the original array. Methods like `.map()`, `.filter()`, and `.sort()` (with spread `[...arr]`) return new arrays instead of modifying the original.

**`.flat()`**
Flattens a nested array by one level.
Example: `[[1, 2], [3, 4]].flat()` → `[1, 2, 3, 4]`

**Template literal**
A string that can include expressions using backticks and `${}`.
Example: `` `Hello, ${name}!` ``

**`.localeCompare()`**
Compares two strings alphabetically, correctly handling special characters.
Used in `.sort()` for string properties.
Example: `a.name.localeCompare(b.name)`

---

**Next step:** Go to `03-exercises.md`.
