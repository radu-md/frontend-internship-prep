# Module 01 — Theory: Internet, HTML, CSS

## What is frontend development?

Frontend development is everything the user **sees and interacts with** in a browser.

When you open a website, you see text, buttons, images, forms, and colors.
All of that is built with **HTML**, **CSS**, and **JavaScript**.

Backend development is everything that happens on the server — the database, the logic behind login, the data processing.
As a frontend developer, you do not need to build the backend. You only need to understand that it exists and that it communicates with your frontend using an **API**.

---

## How does a website work?

1. You type a URL in the browser (example: `https://google.com`)
2. The browser sends a **request** to a server
3. The server sends back a **response** — usually an HTML file
4. The browser reads the HTML and displays the page
5. If the HTML links to CSS files and JavaScript files, the browser loads those too

This is called the **request → response** cycle.

---

## What is HTML?

**HTML** stands for HyperText Markup Language.

HTML gives the page its **structure**.
It tells the browser: here is a title, here is a paragraph, here is a button.

HTML uses **tags**. A tag looks like this:

```html
<p>This is a paragraph.</p>
```

The `<p>` is the opening tag. The `</p>` is the closing tag. The text is the content.

### Common HTML tags

| Tag | What it does |
|---|---|
| `<h1>` to `<h6>` | Headings (h1 is biggest) |
| `<p>` | Paragraph |
| `<a href="...">` | Link |
| `<img src="...">` | Image |
| `<div>` | Generic container block |
| `<span>` | Generic container inline |
| `<ul>` / `<ol>` | Unordered / ordered list |
| `<li>` | List item |
| `<button>` | Clickable button |
| `<input>` | Input field |
| `<form>` | Form container |
| `<label>` | Label for an input |

### HTML page structure

Every HTML page has this basic structure:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello</h1>
    <p>This is my page.</p>
  </body>
</html>
```

- `<head>` — invisible to the user, contains metadata and links to CSS
- `<body>` — everything visible on the page

---

## What is CSS?

**CSS** stands for Cascading Style Sheets.

CSS gives the page its **appearance**.
It tells the browser: make this text blue, make this button rounded, put this image on the left.

CSS uses **selectors** to target HTML elements, then applies **properties**.

```css
p {
  color: blue;
  font-size: 16px;
}
```

This makes all `<p>` elements blue with font size 16px.

### Common CSS selectors

| Selector | What it targets |
|---|---|
| `p` | All `<p>` elements |
| `.card` | All elements with `class="card"` |
| `#title` | The element with `id="title"` |
| `div p` | All `<p>` inside a `<div>` |

### The box model

Every HTML element is a box. The box has four layers:

```
┌─────────────────────────────┐
│          margin             │
│  ┌───────────────────────┐  │
│  │        border         │  │
│  │  ┌─────────────────┐  │  │
│  │  │     padding     │  │  │
│  │  │  ┌───────────┐  │  │  │
│  │  │  │  content  │  │  │  │
│  │  │  └───────────┘  │  │  │
│  │  └─────────────────┘  │  │
│  └───────────────────────┘  │
└─────────────────────────────┘
```

- **content** — the actual text or image
- **padding** — space inside the border
- **border** — line around the element
- **margin** — space outside the border

---

## Flexbox — simple layout

Flexbox makes it easy to arrange elements in a row or column.

```css
.container {
  display: flex;
  flex-direction: row;   /* or column */
  justify-content: center; /* horizontal alignment */
  align-items: center;     /* vertical alignment */
  gap: 16px;               /* space between items */
}
```

Apply `display: flex` to the **parent** element.
The **children** inside will automatically be arranged.

---

## Responsive design

Responsive design means the page looks good on all screen sizes — phone, tablet, desktop.

The main tool is the **media query**:

```css
/* Default: for large screens */
.card {
  width: 400px;
}

/* When screen is smaller than 600px */
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
}
```

Another simple trick is to use `%` or `max-width` instead of fixed pixel widths:

```css
.container {
  max-width: 800px;
  width: 100%;
}
```

---

## Forms

Forms are used to collect input from the user.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter your name" />

  <label for="email">Email:</label>
  <input type="email" id="email" placeholder="Enter your email" />

  <button type="submit">Submit</button>
</form>
```

Common input types: `text`, `email`, `password`, `number`, `checkbox`, `radio`

---

## Summary

| Concept | What it does |
|---|---|
| HTML | Gives the page structure |
| CSS | Gives the page appearance |
| Box model | Every element is a box with content, padding, border, margin |
| Flexbox | Arranges elements in rows or columns |
| Media query | Changes styles for different screen sizes |
| Form | Collects input from the user |

**Next step:** Read `02-terminology.md` to learn the key words for this module.
