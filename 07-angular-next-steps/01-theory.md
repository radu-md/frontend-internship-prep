# Module 07 — Theory: Angular Next Steps

## Services

A **service** is a TypeScript class used to share logic or data between components.

Instead of putting all logic in a component, you move it to a service. This keeps components clean and makes logic reusable.

Common uses:
- Fetching data from an API
- Sharing data between multiple components
- Business logic (calculations, transformations)

```ts
// user.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'  // makes the service available everywhere
})
export class UserService {
  private users = ['Alice', 'Bob', 'Charlie'];

  getUsers(): string[] {
    return this.users;
  }
}
```

---

## Dependency Injection (DI)

Angular automatically creates and provides services to components — this is called **Dependency Injection**.

You declare what you need in the constructor, and Angular provides it:

```ts
import { Component } from '@angular/core';
import { UserService } from './user.service';

@Component({ ... })
export class UserListComponent {
  users: string[] = [];

  constructor(private userService: UserService) {
    this.users = this.userService.getUsers();
  }
}
```

You do not create the service manually — Angular handles it.

---

## Lifecycle hooks

Lifecycle hooks are methods Angular calls at specific moments in a component's life.

The most important one is `ngOnInit`:

```ts
import { Component, OnInit } from '@angular/core';

@Component({ ... })
export class MyComponent implements OnInit {
  data: string[] = [];

  ngOnInit(): void {
    // runs once when the component is created
    // good place to load data
    this.data = ['item1', 'item2'];
  }
}
```

| Hook | When it runs |
|---|---|
| `ngOnInit` | Once, after the component is created |
| `ngOnDestroy` | When the component is removed from the page |
| `ngOnChanges` | When an `@Input` value changes |

Use `ngOnInit` for loading data — not the constructor.

---

## Routing

Routing lets you navigate between different pages (components) without reloading the browser.

### Set up routes

```ts
// app-routing.module.ts
const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'users', component: UserListComponent },
  { path: 'users/:id', component: UserDetailComponent },
  { path: '**', component: NotFoundComponent }  // catch-all
];
```

### Display the current route

```html
<!-- app.component.html -->
<nav>
  <a routerLink="/">Home</a>
  <a routerLink="/users">Users</a>
</nav>

<router-outlet></router-outlet>
```

`<router-outlet>` is where the routed component is displayed.

### Navigate with route params

```ts
// In the template
<a [routerLink]="['/users', user.id]">{{ user.name }}</a>

// In the component receiving the param
import { ActivatedRoute } from '@angular/router';

constructor(private route: ActivatedRoute) {}

ngOnInit(): void {
  const id = this.route.snapshot.paramMap.get('id');
}
```

---

## Component communication

### `@Input` — parent sends data to child

```ts
// child.component.ts
import { Input } from '@angular/core';

export class ChildComponent {
  @Input() title: string = '';
}
```

```html
<!-- parent template -->
<app-child [title]="'Hello from parent'"></app-child>
```

### `@Output` — child sends events to parent

```ts
// child.component.ts
import { Output, EventEmitter } from '@angular/core';

export class ChildComponent {
  @Output() buttonClicked = new EventEmitter<string>();

  onClick(): void {
    this.buttonClicked.emit('Child was clicked!');
  }
}
```

```html
<!-- child template -->
<button (click)="onClick()">Click me</button>

<!-- parent template -->
<app-child (buttonClicked)="onChildClick($event)"></app-child>
```

```ts
// parent component
onChildClick(message: string): void {
  console.log(message);
}
```

---

## Forms

### Template-driven forms

Simpler, good for basic forms.

```html
<form #myForm="ngForm" (ngSubmit)="onSubmit(myForm)">
  <input name="email" ngModel required type="email" />
  <button type="submit">Submit</button>
</form>
```

### Reactive forms

More control, good for complex forms.

```ts
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

export class LoginComponent {
  form: FormGroup;

  constructor(private fb: FormBuilder) {
    this.form = this.fb.group({
      email: ['', [Validators.required, Validators.email]],
      password: ['', [Validators.required, Validators.minLength(6)]]
    });
  }

  onSubmit(): void {
    if (this.form.valid) {
      console.log(this.form.value);
    }
  }
}
```

```html
<form [formGroup]="form" (ngSubmit)="onSubmit()">
  <input formControlName="email" />
  <input formControlName="password" type="password" />
  <button type="submit">Login</button>
</form>
```

---

## HTTP and Observables (basics)

### Making an HTTP request

```ts
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Observable } from 'rxjs';

@Injectable({ providedIn: 'root' })
export class UserService {
  constructor(private http: HttpClient) {}

  getUsers(): Observable<any[]> {
    return this.http.get<any[]>('https://jsonplaceholder.typicode.com/users');
  }
}
```

### Using the service in a component

```ts
export class UserListComponent implements OnInit {
  users: any[] = [];

  constructor(private userService: UserService) {}

  ngOnInit(): void {
    this.userService.getUsers().subscribe(data => {
      this.users = data;
    });
  }
}
```

**What is an Observable?**
An Observable is like a stream — it delivers data over time. You use `.subscribe()` to receive that data.
Think of it like: "When the data is ready, give it to me."

Import `HttpClientModule` in your app module (or `provideHttpClient()` in newer Angular) to use `HttpClient`.

---

## Summary

| Concept | Purpose |
|---|---|
| Service | Shared logic and data |
| `@Injectable` | Marks a class as a service |
| DI (Dependency Injection) | Angular provides services automatically via constructor |
| `ngOnInit` | Lifecycle hook — runs once after component is created |
| Routing | Navigate between components/pages |
| `<router-outlet>` | Where routed components are displayed |
| `routerLink` | Navigation link (no page reload) |
| `@Input` | Parent passes data to child |
| `@Output` + `EventEmitter` | Child sends events to parent |
| Observable | Async data stream — use `.subscribe()` to receive data |

**Next step:** Go to `02-exercises.md`.
