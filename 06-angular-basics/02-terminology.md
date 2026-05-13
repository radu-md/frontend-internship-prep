# Module 06 — Terminology: Angular Basics

Learn these words. These will come up in interviews.

---

## Core Angular concepts

**Angular**
A frontend framework made by Google for building Single Page Applications.
Uses TypeScript, components, templates, and a module system.

**Framework**
A set of tools and rules that help you build applications in a structured way.
Unlike a library, a framework controls the overall structure.

**SPA (Single Page Application)**
A web app where the page does not fully reload when you navigate.
JavaScript updates the content on screen instead.
Example: Gmail, Google Maps.

**Angular CLI**
Command Line Interface for Angular. Used to create projects, generate components, and run the app.
Key command: `ng new`, `ng serve`, `ng generate component`

**Component**
The basic building block of an Angular app.
Each component has: a TypeScript class (logic), an HTML template (view), and a CSS file (styles).

**Decorator**
A special annotation that gives Angular information about a class.
Example: `@Component({...})` tells Angular "this class is a component".

**Selector**
The HTML tag name used to insert a component into a template.
Example: `selector: 'app-header'` → used as `<app-header></app-header>`

**Template**
The HTML file (or inline HTML) that defines what a component displays.

**Module**
A container that groups related components, directives, pipes, and services.
The root module is `AppModule` (in older Angular with `app.module.ts`).

---

## Data binding

**Interpolation**
Showing component data in the template using `{{ }}`.
Example: `{{ userName }}` displays the value of `userName`.

**Data binding**
The connection between component data and the template.
Changes in one reflect in the other.

**Property binding**
Binding a component value to an HTML element's attribute.
Syntax: `[src]="imageUrl"`

**Event binding**
Listening for a user action (click, input, etc.) and calling a method.
Syntax: `(click)="doSomething()"`

**Two-way binding**
Combining property and event binding so the input and the component stay in sync.
Syntax: `[(ngModel)]="username"`
Requires `FormsModule`.

---

## Directives and pipes

**Directive**
An Angular instruction that modifies the DOM.
Examples: `*ngIf`, `*ngFor`

**`*ngIf`**
A structural directive that shows or hides an element based on a condition.
Example: `<p *ngIf="isVisible">Hello</p>`

**`*ngFor`**
A structural directive that repeats an element for each item in a list.
Example: `<li *ngFor="let item of items">{{ item }}</li>`

**Structural directive**
A directive that changes the structure of the DOM (adds or removes elements).
Marked with `*` in the template.

**Pipe**
Transforms a value for display in the template.
Example: `{{ name | uppercase }}` → displays the name in all caps.

---

## Common pipes

| Pipe | Example | Output |
|---|---|---|
| `uppercase` | `{{ 'hello' \| uppercase }}` | HELLO |
| `lowercase` | `{{ 'HELLO' \| lowercase }}` | hello |
| `currency` | `{{ 29.9 \| currency }}` | $29.90 |
| `date` | `{{ today \| date }}` | May 13, 2026 |
| `slice` | `{{ 'hello world' \| slice:0:5 }}` | hello |

---

**Next step:** Go to `03-exercises.md`.
