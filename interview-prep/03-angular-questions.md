# Interview Prep — Angular Questions

Common Angular interview questions for a beginner/intern level.

Read the question, try to answer in your own words, then check the model answer.

---

## What is Angular?

**Model answer:**
> "Angular is a frontend framework made by Google for building Single Page Applications. It uses TypeScript and gives you a structured way to build reusable components, manage data, handle routing, and communicate with a backend."

---

## What is a component?

**Model answer:**
> "A component is the basic building block of an Angular app. It has three parts: a TypeScript class that contains the logic, an HTML template that defines what is displayed, and a CSS file for styling. Components can be nested — one component can contain other components."

---

## What is a service?

**Model answer:**
> "A service is a TypeScript class used to share logic or data across components. For example, instead of each component making its own HTTP request, one service does it and multiple components can use it."

---

## What is Dependency Injection?

**Model answer:**
> "Dependency Injection is how Angular provides services to components. Instead of creating a service manually, I declare it as a constructor parameter and Angular creates and injects it automatically. This makes components easier to test and reuse."

---

## What is data binding?

**Model answer:**
> "Data binding is the connection between the component and the template. There are 4 types:
> - Interpolation `{{ }}` — shows data in the template
> - Property binding `[property]` — binds data to an HTML attribute
> - Event binding `(event)` — listens for user actions
> - Two-way binding `[(ngModel)]` — syncs input with a property in both directions"

---

## What is the difference between `*ngIf` and `*ngFor`?

**Model answer:**
> "`*ngIf` shows or hides an element based on a condition. `*ngFor` repeats an element for each item in a list. Both are structural directives — they change the structure of the DOM."

---

## What is routing in Angular?

**Model answer:**
> "Routing lets you navigate between different views or pages without reloading the browser. You define routes that map URL paths to components, and use `<router-outlet>` to display the active component. Navigation links use `routerLink` instead of `href`."

---

## What is `ngOnInit` and when does it run?

**Model answer:**
> "`ngOnInit` is a lifecycle hook that runs once after the component is created. It is the right place to load data — for example, calling a service to fetch from an API. The constructor should be kept simple."

---

## What is the difference between `@Input` and `@Output`?

**Model answer:**
> "`@Input` is how a parent component passes data down to a child component. `@Output` is how a child component sends events up to a parent, using `EventEmitter`."

---

## What is a pipe?

**Model answer:**
> "A pipe transforms a value for display in the template. For example, `{{ name | uppercase }}` displays the name in all capitals. Angular has built-in pipes like `currency`, `date`, `slice`, and you can create custom ones."

---

## What is the difference between template-driven and reactive forms?

**Model answer:**
> "Template-driven forms are simpler — you define most of the form logic in the HTML template using `ngModel`. Reactive forms give you more control — you define the form structure in TypeScript using `FormGroup` and `FormControl`, which makes validation and dynamic forms easier to manage."

---

## What is an Observable?

**Model answer:**
> "An Observable is a way to handle asynchronous data — data that arrives over time. In Angular, HTTP calls return Observables. You use `.subscribe()` to receive the data when it arrives. It is similar to a Promise but more powerful because it can emit multiple values."

---

## What is a directive?

**Model answer:**
> "A directive is an instruction that changes the behavior or structure of the DOM. Structural directives like `*ngIf` and `*ngFor` add or remove elements. Attribute directives like `ngClass` or `ngStyle` change the appearance of existing elements."

---

## What is `<router-outlet>`?

**Model answer:**
> "`<router-outlet>` is a placeholder in the template where Angular renders the component that matches the current route. You put it in the root component's template, and it updates automatically when the route changes."
