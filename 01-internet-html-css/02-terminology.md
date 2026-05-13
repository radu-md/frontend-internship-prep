# Module 01 — Terminology: Internet, HTML, CSS

Learn these words. Try to explain each one in your own words after reading.

---

## Internet and web

**Frontend**
The part of a website the user sees and interacts with.
Example: buttons, forms, text, images on a page.

**Backend**
The part that runs on the server. Handles data, login logic, databases.
Example: when you submit a form, the backend saves the data.

**Browser**
The app you use to open websites.
Example: Chrome, Firefox, Edge.

**Server**
A computer that stores website files and sends them to the browser when requested.

**Request**
A message sent from the browser to the server asking for something.
Example: "give me the homepage".

**Response**
The message the server sends back to the browser.
Example: an HTML file with the page content.

**URL**
The address of a page on the internet.
Example: `https://github.com`

**API**
A way for the frontend to communicate with the backend.
The frontend sends a request, the API returns data (usually JSON).

**HTTP / HTTPS**
The protocol used to send requests and responses over the internet.
HTTPS is the secure version.

---

## HTML

**HTML**
HyperText Markup Language. Defines the structure of a web page.

**Tag**
An HTML instruction wrapped in angle brackets.
Example: `<p>`, `<h1>`, `<div>`

**Element**
A complete HTML unit — opening tag, content, closing tag.
Example: `<p>Hello</p>`

**Attribute**
Extra information added inside a tag.
Example: `<a href="https://google.com">` — `href` is the attribute.

**`id`**
A unique name given to one specific element.
Example: `<div id="header">` — only one element should have this id.

**`class`**
A name given to one or more elements for styling.
Example: `<div class="card">` — many elements can share a class.

**`<div>`**
A generic block container with no visual style by default.
Used to group elements together.

**`<span>`**
A generic inline container. Used to style part of text.

**Semantic HTML**
Using HTML tags that describe their meaning.
Example: `<header>`, `<nav>`, `<main>`, `<footer>` instead of all `<div>`.

---

## CSS

**CSS**
Cascading Style Sheets. Controls how the page looks — colors, sizes, layout.

**Selector**
The part of CSS that targets which element to style.
Example: `p` targets all paragraphs. `.card` targets elements with class "card".

**Property**
What you want to change.
Example: `color`, `font-size`, `margin`, `padding`

**Value**
The setting for the property.
Example: `color: blue;`, `font-size: 16px;`

**Box model**
Every element is treated as a box with: content → padding → border → margin.

**Padding**
Space between the content and the border. Inside the element.

**Margin**
Space outside the border. Between this element and others.

**Border**
The line around an element.
Example: `border: 1px solid black;`

**Flexbox**
A CSS layout system. Makes it easy to arrange elements in rows or columns.
Applied with `display: flex` on the parent container.

**`justify-content`**
Controls horizontal alignment in a flex container.
Example: `justify-content: center` centers items horizontally.

**`align-items`**
Controls vertical alignment in a flex container.
Example: `align-items: center` centers items vertically.

**Responsive design**
Making the page work well on different screen sizes (phone, tablet, desktop).

**Media query**
A CSS rule that applies styles only when the screen matches certain conditions.
Example: `@media (max-width: 600px) { ... }` — applies when screen is 600px or smaller.

---

## Quick reference: id vs class

| | `id` | `class` |
|---|---|---|
| How many per page | Only one | Many |
| CSS selector | `#myId` | `.myClass` |
| Use for | Unique elements | Reusable styles |

**Next step:** Go to `03-exercises.md` and practice what you learned.
