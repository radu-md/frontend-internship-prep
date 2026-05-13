# Module 05 — Exercises: TypeScript and OOP

Write your solutions in `.ts` files or use the TypeScript playground: https://www.typescriptlang.org/play

---

## Exercise 1 — Type annotations

Rewrite these JavaScript variables with TypeScript type annotations:

```js
let username = 'Alex';
let score = 95;
let isLoggedIn = false;
let tags = ['beginner', 'frontend', 'angular'];
```

Then add one more variable for each type and verify TypeScript accepts it.

---

## Exercise 2 — Interface

Create a `Product` interface with these properties:
- `id` — number
- `name` — string
- `price` — number
- `category` — string
- `description` — optional string

Then create 3 product objects that use this interface.

---

## Exercise 3 — User class

Create a `User` class with:
- Properties: `name` (public), `email` (public), `password` (private)
- A constructor that sets all three
- A method `greet()` that returns: `"Hello, I am [name]"`
- A method `changePassword(newPassword: string)` that updates the private password

Create 2 user objects and call their methods.

---

## Exercise 4 — Product class

Create a `Product` class with:
- Properties: `name`, `price`, `stock` (all public)
- A constructor that sets all three
- A method `isAvailable()` that returns `true` if stock > 0
- A method `applyDiscount(percent: number)` that reduces the price by that percentage

Example:
```ts
const laptop = new Product('Laptop', 1000, 5);
console.log(laptop.isAvailable());       // true
laptop.applyDiscount(10);
console.log(laptop.price);               // 900
```

---

## Exercise 5 — Inheritance

Create a base class `Animal` with:
- Property: `name`
- Method: `speak()` that returns `"[name] makes a sound."`

Create two child classes:
- `Dog` — overrides `speak()` to return `"[name] barks!"`
- `Cat` — overrides `speak()` to return `"[name] meows!"`

Create one object of each and call `speak()`.

---

## Exercise 6 — Shopping cart

Create three classes:

1. `CartItem`:
   - Properties: `name` (string), `price` (number), `quantity` (number)
   - Method `total()` → returns `price * quantity`

2. `Cart`:
   - Property: `items` — an array of `CartItem` objects (start empty)
   - Method `addItem(item: CartItem)` — adds item to the array
   - Method `getTotal()` — returns the sum of all item totals
   - Method `getCount()` — returns the total number of items

3. Use it:
```ts
const cart = new Cart();
cart.addItem(new CartItem('Laptop', 999, 1));
cart.addItem(new CartItem('Mouse', 29, 2));

console.log(cart.getTotal());  // 1057
console.log(cart.getCount());  // 3
```

---

**Next step:** Go to `04-validation.md`.
