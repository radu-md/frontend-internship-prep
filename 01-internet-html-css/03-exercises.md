# Module 01 — Exercises: Internet, HTML, CSS

Complete each exercise in order.
Read the goal, then write the code yourself.
Do not copy — try first, then look at hints if needed.

---

## Exercise 1 — Personal profile page

**Goal:** Build a simple personal profile page using HTML and CSS.

**Requirements:**
- A heading with a name
- A short paragraph describing the person (2–3 sentences)
- An unordered list with 3 hobbies or skills
- A link to any website
- Basic CSS: background color, text color, centered content, some padding

**Starter file:** Create a file called `profile.html`

**Hint — HTML structure to get started:**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Profile</title>
    <style>
      /* your CSS here */
    </style>
  </head>
  <body>
    <!-- your HTML here -->
  </body>
</html>
```

**Check yourself:**
- Does the page have a heading, paragraph, and list?
- Does the CSS change at least 2 visual things?
- Does the link open a page when clicked?

---

## Exercise 2 — Login form

**Goal:** Build a login form UI using HTML and CSS.

**Requirements:**
- A heading: "Login"
- An email input field with a label
- A password input field with a label
- A submit button that says "Log In"
- CSS: form centered on the page, inputs have padding and border, button has background color

**Create a file:** `login.html`

**Hint — form structure:**
```html
<form>
  <label for="email">Email</label>
  <input type="email" id="email" placeholder="your@email.com" />

  <label for="password">Password</label>
  <input type="password" id="password" placeholder="Your password" />

  <button type="submit">Log In</button>
</form>
```

**Check yourself:**
- Are both inputs correctly typed (`email`, `password`)?
- Does each input have a matching label?
- Does the button say "Log In"?
- Is the form visually styled (not plain browser default)?

---

## Exercise 3 — Product card

**Goal:** Build a product card UI using HTML and CSS.

**Requirements:**
- A card with: product name, short description, price, and a "Buy" button
- CSS: card has a border or shadow, rounded corners, padding
- The card should look centered on the page

**Create a file:** `product-card.html`

**Hint — card structure:**
```html
<div class="card">
  <h2>Product Name</h2>
  <p>Short description of the product.</p>
  <p class="price">$29.99</p>
  <button>Buy</button>
</div>
```

**Hint — basic card CSS:**
```css
.card {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 24px;
  max-width: 300px;
  margin: 40px auto;
}
```

**Check yourself:**
- Does the card have all 4 parts: name, description, price, button?
- Does the card have visible styling (not just plain text)?
- Does the card look centered?

---

## Exercise 4 — Flexbox row

**Goal:** Use Flexbox to display 3 product cards in a row.

**Requirements:**
- Create 3 simple card elements
- Use `display: flex` on a container to put them side by side
- Add a gap between cards
- On small screens (max-width 600px), cards should stack vertically

**Hint — flex container:**
```css
.cards-container {
  display: flex;
  flex-direction: row;
  gap: 16px;
}

@media (max-width: 600px) {
  .cards-container {
    flex-direction: column;
  }
}
```

**Check yourself:**
- Do the 3 cards appear side by side on a wide screen?
- Do they stack on a narrow screen (you can test by resizing the browser window)?

---

**Next step:** Go to `04-mini-challenge.md` when all exercises are done.
