# Module 03 — Exercises: JavaScript DOM

Write your code in `.html` files with a `<script>` tag, or use the browser console.

---

## Part A — DOM exercises

### Exercise 1 — Select and change

Create an HTML page with:
- A heading with `id="title"` that says "Hello"
- A paragraph with `id="description"` that says "This is the description."
- A button that says "Change Text"

When the button is clicked:
- Change the heading text to "Welcome!"
- Change the paragraph text to "Text has been updated."
- Change the heading color to blue

---

### Exercise 2 — Show and hide

Create a page with:
- A paragraph with some text
- A button that says "Toggle"

When the button is clicked:
- If the paragraph is visible, hide it
- If the paragraph is hidden, show it

**Hint:** Use `classList.toggle()` and a CSS class:
```css
.hidden { display: none; }
```

---

### Exercise 3 — Input and display

Create a page with:
- A text input field
- A button "Add"
- An empty `<ul>` list

When the user types something and clicks "Add":
- Create a new `<li>` with the input text
- Add it to the list
- Clear the input field

---

### Exercise 4 — Form with validation

Create a login form with:
- Email input
- Password input
- Submit button
- An empty `<p id="message">` for feedback

When submitted:
- If email is empty → show "Email is required"
- If password is shorter than 6 characters → show "Password too short"
- If both are valid → show "Login successful!"
- Use `event.preventDefault()` to stop page reload

---

### Exercise 5 — localStorage

Create a page with:
- A text input
- A "Save" button
- A "Load" button
- A `<p>` to display the saved text

When "Save" is clicked: save the input value to `localStorage`
When "Load" is clicked: read from `localStorage` and show it in the `<p>`

The saved value should still be there after refreshing the page.

---

## Part B — Beginner algorithm exercises

Write each as a JavaScript function. Test it by calling it with different inputs and logging the result.

### Algorithm 1 — Reverse a string
```
Input: 'hello'
Output: 'olleh'
```

### Algorithm 2 — Find the largest number
```
Input: [3, 7, 1, 9, 4]
Output: 9
```

### Algorithm 3 — Count words
```
Input: 'the quick brown fox'
Output: 4
```

Hint: use `.split(' ')`

### Algorithm 4 — Remove duplicates
```
Input: [1, 2, 2, 3, 3, 3, 4]
Output: [1, 2, 3, 4]
```

Hint: use `filter` with `indexOf`, or look up how `Set` works.

### Algorithm 5 — Sum all numbers
```
Input: [1, 2, 3, 4, 5]
Output: 15
```

Hint: use a loop or look up `reduce`.

### Algorithm 6 — Find even numbers
```
Input: [1, 2, 3, 4, 5, 6]
Output: [2, 4, 6]
```

---

**Next step:** Go to `03-mini-challenge.md`.
