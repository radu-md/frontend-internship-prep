# Module 03 — Theory: JavaScript DOM

## What is the DOM?

When the browser loads an HTML page, it creates a tree of objects from the HTML.
This tree is called the **DOM** — Document Object Model.

JavaScript can read and change this tree — that is how pages become interactive.

Think of it this way:
- HTML is the structure written in a file
- DOM is the live version of that structure in the browser
- JavaScript talks to the DOM to make changes happen

---

## Selecting elements

To work with an HTML element, you first need to find it.

```js
// Select by id
const title = document.getElementById('title');

// Select by CSS selector (more flexible)
const button = document.querySelector('button');
const card = document.querySelector('.card');
const heading = document.querySelector('#main-heading');

// Select all matching elements (returns a list)
const allItems = document.querySelectorAll('.item');
```

---

## Changing content and style

Once you have an element, you can change it:

```js
const title = document.querySelector('h1');

// Change text
title.textContent = 'New title';

// Change HTML inside (careful with this)
title.innerHTML = '<span>New title</span>';

// Change CSS style
title.style.color = 'blue';
title.style.fontSize = '24px';

// Add or remove a CSS class
title.classList.add('active');
title.classList.remove('active');
title.classList.toggle('active');  // add if not there, remove if it is
```

---

## Events

An event happens when the user does something — clicks, types, submits a form, etc.

You listen for events with `addEventListener`:

```js
const button = document.querySelector('button');

button.addEventListener('click', function() {
  console.log('Button clicked!');
});

// Arrow function version (same result)
button.addEventListener('click', () => {
  console.log('Button clicked!');
});
```

### Common events

| Event | When it fires |
|---|---|
| `click` | User clicks an element |
| `input` | User types in an input field |
| `submit` | User submits a form |
| `keydown` | User presses a key |
| `mouseover` | User hovers over an element |

---

## Form handling

```html
<form id="login-form">
  <input type="text" id="username" />
  <button type="submit">Submit</button>
</form>
```

```js
const form = document.querySelector('#login-form');

form.addEventListener('submit', function(event) {
  event.preventDefault();  // stop the page from reloading

  const username = document.querySelector('#username').value;
  console.log('Submitted:', username);
});
```

`event.preventDefault()` is important — without it, the form submission reloads the page.

---

## Creating and adding elements

```js
// Create a new element
const newItem = document.createElement('li');
newItem.textContent = 'New task';

// Add it to an existing element
const list = document.querySelector('#task-list');
list.appendChild(newItem);

// Remove an element
newItem.remove();
```

---

## localStorage

`localStorage` lets you save small amounts of data in the browser.
The data stays even after the page is closed.

```js
// Save a value
localStorage.setItem('username', 'Alex');

// Read a value
const name = localStorage.getItem('username');  // 'Alex'

// Remove a value
localStorage.removeItem('username');

// Clear everything
localStorage.clear();
```

For saving objects or arrays, use JSON:

```js
// Save an array
const tasks = ['buy milk', 'read book'];
localStorage.setItem('tasks', JSON.stringify(tasks));

// Read it back
const saved = JSON.parse(localStorage.getItem('tasks'));
```

---

## async / await

Some operations take time — like loading data from a server.
`async/await` lets you handle these without blocking the rest of the code.

```js
async function loadUser() {
  const response = await fetch('https://jsonplaceholder.typicode.com/users/1');
  const user = await response.json();
  console.log(user.name);
}

loadUser();
```

- `async` before a function means it will handle async operations
- `await` pauses inside that function until the operation finishes
- `fetch()` is a built-in browser function to load data from a URL

### Error handling with try/catch

```js
async function loadUser() {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/users/1');
    const user = await response.json();
    console.log(user.name);
  } catch (error) {
    console.log('Something went wrong:', error.message);
  }
}
```

---

## Browser DevTools

Open DevTools with `F12` (or right-click → Inspect).

Key tabs:
- **Console** — see `console.log()` output and errors
- **Elements** — inspect and edit HTML/CSS live
- **Network** — see requests and responses
- **Sources** — view and debug JavaScript files

Use `console.log()` often while building — it is your best debugging tool.

---

## Beginner algorithms (Week 3)

You will practice these in `02-exercises.md`:

- Reverse a string
- Find the largest number in an array
- Count words in a sentence
- Remove duplicates from an array
- Sum all numbers in an array
- Find even numbers

These are simple logic exercises — not complex math.
The goal is to practice thinking step by step.

---

## Summary

| Concept | Key point |
|---|---|
| DOM | The live tree of HTML elements in the browser |
| `querySelector` | Find an element by CSS selector |
| `textContent` | Get or set the text of an element |
| `classList` | Add, remove, toggle CSS classes |
| `addEventListener` | Listen for user actions |
| `event.preventDefault()` | Stop default form submit behavior |
| `localStorage` | Save data in the browser between sessions |
| `async/await` | Handle operations that take time |
| `try/catch` | Handle errors in async code |

**Next step:** Go to `02-exercises.md`.
