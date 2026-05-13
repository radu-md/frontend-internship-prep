# Module 07 — Exercises: Angular Next Steps

---

## Exercise 1 — Create and use a service

**Goal:** Move data out of a component into a service.

1. Generate a service: `ng generate service product`
2. In the service, create a `products` array with at least 4 items:
   ```ts
   { id: number, name: string, price: number }
   ```
3. Add a `getProducts()` method that returns the array
4. Inject the service into a component
5. In `ngOnInit`, call `getProducts()` and store the result
6. Display the products in the template using `*ngFor`

---

## Exercise 2 — Set up routing

**Goal:** Create 2 pages and navigate between them.

1. Create two components: `HomeComponent` and `AboutComponent`
2. Set up routes:
   - `/` → `HomeComponent`
   - `/about` → `AboutComponent`
3. In `app.component.html`:
   - Add navigation links using `routerLink`
   - Add `<router-outlet>`
4. Verify that clicking the links changes the displayed component without reloading the page

---

## Exercise 3 — Route with parameter

**Goal:** Navigate to a detail page and read the URL param.

1. Create a `UserDetailComponent`
2. Add route: `/users/:id`
3. In the component, use `ActivatedRoute` to read the `id` from the URL
4. Display the id on the page: "Viewing user #[id]"
5. On the users list, add a link for each user that navigates to `/users/[id]`

---

## Exercise 4 — @Input and @Output

**Goal:** Pass data between a parent and child component.

1. Create a `ProductCardComponent` with:
   - `@Input() product: { name: string, price: number }`
   - `@Output() addToCart = new EventEmitter()`
   - Template: shows name, price, and an "Add to Cart" button
   - On button click, emit the event

2. In a parent component:
   - Create a products array
   - Use `*ngFor` to render `<app-product-card>` for each product
   - Listen to the `(addToCart)` event and log the product

---

## Exercise 5 — Reactive form

**Goal:** Build a login form with validation using reactive forms.

1. Create a `LoginComponent`
2. Build a `FormGroup` with:
   - `email` — required, must be email format
   - `password` — required, minimum 6 characters
3. Template:
   - Email input with `formControlName="email"`
   - Password input with `formControlName="password"`
   - Submit button (disabled when form is invalid)
   - Error messages (use `*ngIf`):
     - Show "Email is required" if email is touched and empty
     - Show "Password too short" if password is touched and too short
4. On submit (if valid): log the form values

---

## Exercise 6 — HTTP request

**Goal:** Load data from a public API and display it.

1. Create a service `JsonPlaceholderService`
2. Inject `HttpClient`
3. Add a method `getUsers()` that calls:
   `https://jsonplaceholder.typicode.com/users`
4. In a component, call the service in `ngOnInit` and store the users
5. Display each user's `name` and `email` in the template
6. While loading, show a "Loading..." message (use a `isLoading` boolean)

---

**Next step:** Go to `03-mini-challenge.md`.
