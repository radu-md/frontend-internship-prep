# Module 02 — Mini Challenge: JavaScript Basics

This is a bigger task that combines everything from this module.

Plan your solution before writing code.

---

## Challenge: Product filter app (plain JavaScript)

**Goal:** Build a simple product filtering page using HTML + JavaScript.

---

## What to build

A page that shows a list of products and lets the user filter them by category.

### Data

Use this product list in your JavaScript:

```js
const products = [
  { name: 'Laptop', price: 999, category: 'electronics' },
  { name: 'T-Shirt', price: 25, category: 'clothing' },
  { name: 'Phone', price: 699, category: 'electronics' },
  { name: 'Jeans', price: 59, category: 'clothing' },
  { name: 'Headphones', price: 149, category: 'electronics' },
  { name: 'Sneakers', price: 89, category: 'clothing' },
  { name: 'Tablet', price: 349, category: 'electronics' }
];
```

### Features to build

1. **Display all products** on the page when it loads
   - Show: product name, price, category

2. **Filter buttons** — 3 buttons: "All", "Electronics", "Clothing"
   - Clicking a button filters the list to show only that category
   - "All" shows every product

3. **Product count** — show how many products are currently visible
   - Example: "Showing 4 products"

---

## HTML starter

```html
<!DOCTYPE html>
<html>
<head>
  <title>Product Filter</title>
  <style>
    /* add your styles here */
  </style>
</head>
<body>
  <h1>Products</h1>

  <div id="filters">
    <button onclick="filterProducts('all')">All</button>
    <button onclick="filterProducts('electronics')">Electronics</button>
    <button onclick="filterProducts('clothing')">Clothing</button>
  </div>

  <p id="count"></p>

  <div id="product-list"></div>

  <script>
    // your JavaScript here
  </script>
</body>
</html>
```

---

## Steps to solve

1. Write the product array
2. Write a `renderProducts(list)` function that:
   - Clears the `#product-list` div
   - Loops through `list` and creates an element for each product
   - Updates the `#count` text with how many products are shown
3. Write the `filterProducts(category)` function that:
   - Filters the array (or shows all if category is `'all'`)
   - Calls `renderProducts()` with the filtered result
4. Call `renderProducts(products)` on page load to show everything

---

## Checklist before finishing

- [ ] All products are shown on load
- [ ] "Electronics" button shows only electronics
- [ ] "Clothing" button shows only clothing
- [ ] "All" button shows everything again
- [ ] Product count updates when filter changes
- [ ] No errors in browser console

---

**Next step:** When done, go to `05-validation.md`.
