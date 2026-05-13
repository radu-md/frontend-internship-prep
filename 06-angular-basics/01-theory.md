# Module 06 — Theory: Angular Basics

## What is Angular?

Angular is a **frontend framework** built by Google.

A framework gives you a structure and set of tools to build applications. Instead of writing everything yourself, Angular provides ready-made patterns for:
- Building reusable UI pieces (components)
- Connecting data to the template (data binding)
- Navigating between pages (routing)
- Communicating with a backend (HTTP)

Angular uses **TypeScript**, which is why Module 05 came first.

Angular is a **Single Page Application (SPA)** framework — the page does not reload when you navigate. Instead, JavaScript updates what is shown on screen.

---

## Angular CLI

The Angular CLI (Command Line Interface) is a tool that creates and manages Angular projects.

```bash
# Install the CLI (done once)
npm install -g @angular/cli

# Create a new project
ng new my-app

# Start the development server
cd my-app
ng serve

# Generate a new component
ng generate component my-component
# or short form:
ng g c my-component
```

After `ng serve`, open `http://localhost:4200` in your browser.

---

## Project structure (key files)

```
my-app/
├── src/
│   ├── app/
│   │   ├── app.component.ts       ← root component logic
│   │   ├── app.component.html     ← root component template
│   │   ├── app.component.css      ← root component styles
│   │   └── app.module.ts          ← registers components (older Angular)
│   ├── main.ts                    ← entry point
│   └── index.html                 ← the single HTML page
├── angular.json                   ← project configuration
└── package.json                   ← dependencies
```

---

## Components

A **component** is the building block of an Angular app.

Every component has 3 parts:
1. **TypeScript class** — logic and data
2. **HTML template** — what is displayed
3. **CSS file** — styles for this component

```ts
// hello.component.ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-hello',
  templateUrl: './hello.component.html',
  styleUrls: ['./hello.component.css']
})
export class HelloComponent {
  name = 'Alex';
  count = 0;

  increment() {
    this.count++;
  }
}
```

```html
<!-- hello.component.html -->
<h1>Hello, {{ name }}!</h1>
<p>Count: {{ count }}</p>
<button (click)="increment()">Add</button>
```

The `selector` (`app-hello`) is how you use this component in other templates:
```html
<app-hello></app-hello>
```

---

## Interpolation

Interpolation shows component data in the template using `{{ }}`.

```ts
title = 'My App';
price = 29.99;
```

```html
<h1>{{ title }}</h1>
<p>Price: {{ price }}</p>
<p>{{ 2 + 2 }}</p>  <!-- you can also write expressions -->
```

---

## Property binding

Bind a component property to an HTML attribute using `[ ]`.

```ts
imageUrl = 'https://example.com/photo.jpg';
isDisabled = true;
```

```html
<img [src]="imageUrl" />
<button [disabled]="isDisabled">Click me</button>
```

---

## Event binding

Listen for user events using `( )`.

```ts
onClick() {
  console.log('Button was clicked');
}
```

```html
<button (click)="onClick()">Click me</button>
<input (input)="onType($event)" />
```

---

## Two-way binding

Two-way binding connects an input field to a component property — changes in the input update the property, and changes to the property update the input.

```ts
username = '';
```

```html
<input [(ngModel)]="username" />
<p>Hello, {{ username }}</p>
```

Requires `FormsModule` to be imported in your module or component.

---

## Directives

Directives are special Angular instructions in HTML templates.

### `*ngIf` — show or hide

```html
<p *ngIf="isLoggedIn">Welcome back!</p>
<p *ngIf="!isLoggedIn">Please log in.</p>
```

### `*ngFor` — loop and display a list

```ts
products = ['Laptop', 'Phone', 'Tablet'];
```

```html
<ul>
  <li *ngFor="let product of products">{{ product }}</li>
</ul>
```

With index:
```html
<li *ngFor="let item of items; let i = index">{{ i + 1 }}. {{ item }}</li>
```

---

## Pipes

Pipes transform data for display in the template.

```html
<p>{{ name | uppercase }}</p>          <!-- Alex -->
<p>{{ price | currency }}</p>          <!-- $29.99 -->
<p>{{ today | date:'dd/MM/yyyy' }}</p> <!-- 13/05/2026 -->
<p>{{ description | slice:0:50 }}</p>  <!-- first 50 chars -->
```

---

## Summary

| Concept | Syntax | What it does |
|---|---|---|
| Interpolation | `{{ value }}` | Shows data in template |
| Property binding | `[property]="value"` | Binds data to HTML attribute |
| Event binding | `(event)="method()"` | Listens for user actions |
| Two-way binding | `[(ngModel)]="value"` | Syncs input with property |
| `*ngIf` | `*ngIf="condition"` | Shows/hides element |
| `*ngFor` | `*ngFor="let item of list"` | Repeats element for each item |
| Pipe | `{{ value \| pipeName }}` | Transforms display value |

**Next step:** Read `02-terminology.md`.
