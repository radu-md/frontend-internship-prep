# Module 06 — Exercises: Angular Basics

For each exercise, generate a new component with `ng generate component [name]`.

---

## Exercise 1 — Counter component

**Goal:** Build a counter that increases and decreases.

Create a `CounterComponent` with:
- A number property `count` starting at 0
- A button "+ Add" that increases count by 1
- A button "- Remove" that decreases count by 1 (minimum 0)
- Display the current count on screen

Use **event binding** for the buttons and **interpolation** for the count.

---

## Exercise 2 — Product list

**Goal:** Display a list of products using `*ngFor`.

Create a `ProductListComponent` with:
- An array of product objects: `{ name: string, price: number }`
- Use `*ngFor` to display each product as a list item
- Show the product name and price
- Format the price with the `currency` pipe

---

## Exercise 3 — Conditional display

**Goal:** Show and hide content using `*ngIf`.

Create a `ToggleComponent` with:
- A boolean property `isVisible` (start as `true`)
- A paragraph with some text, shown only when `isVisible` is true
- A button "Show / Hide" that toggles `isVisible`
- A message "Nothing to show" displayed when `isVisible` is false

---

## Exercise 4 — Name input with two-way binding

**Goal:** Use `[(ngModel)]` to connect an input to a component property.

Create a `GreetingComponent` with:
- A text input bound to a `name` property
- Below the input, show: "Hello, [name]!" using interpolation
- The greeting updates instantly as the user types

Remember to import `FormsModule` in your app module or component.

---

## Exercise 5 — User profile card

**Goal:** Build a profile card using property binding and interpolation.

Create a `ProfileCardComponent` with these properties:
```ts
fullName = 'Alex';
jobTitle = 'Frontend Developer Intern';
avatarUrl = 'https://i.pravatar.cc/100';
isOnline = true;
```

Display:
- The avatar using `[src]="avatarUrl"`
- The full name and job title
- A status badge: "Online" (green) if `isOnline`, "Offline" (gray) if not — use `*ngIf`

---

## Exercise 6 — Pipe practice

**Goal:** Use multiple pipes in one template.

Create a component with these properties:
```ts
productName = 'laptop computer';
price = 1299.5;
releaseDate = new Date();
description = 'This is a very long product description that goes on for many words.';
```

Display each one with the appropriate pipe:
- `productName` → uppercase
- `price` → currency
- `releaseDate` → date (formatted as day/month/year)
- `description` → sliced to the first 30 characters with "..." added after

---

**Next step:** Go to `04-mini-challenge.md`.
