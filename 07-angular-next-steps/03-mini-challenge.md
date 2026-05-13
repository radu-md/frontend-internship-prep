# Module 07 — Mini Challenge: Angular Next Steps

---

## Challenge: Users Directory App

**Goal:** Build a small Angular app that loads a list of users from a public API, displays them, and shows a detail page for each user.

---

## What to build

### Page 1 — Users list (`/users`)
- Fetches users from: `https://jsonplaceholder.typicode.com/users`
- Displays each user as a card with: name, email, city
- A "View Details" button or link for each user
- Show "Loading..." while data is being fetched

### Page 2 — User detail (`/users/:id`)
- Fetches one user from: `https://jsonplaceholder.typicode.com/users/:id`
- Displays: name, email, phone, website, company name
- A "Back to list" link

### Navigation
- A navigation bar with links to Home and Users

---

## Architecture

```
app/
├── services/
│   └── user.service.ts         ← HTTP calls
├── components/
│   ├── user-list/              ← displays the list
│   ├── user-detail/            ← displays one user
│   └── user-card/              ← reusable card (@Input: user)
└── app-routing.module.ts       ← routes
```

---

## Requirements

- Use a `UserService` for all HTTP calls
- Use `@Input` on `UserCardComponent` to receive user data
- Use `ngOnInit` to load data
- Use `ActivatedRoute` to get the `:id` from the URL
- Use `*ngFor` for the list
- Use `*ngIf` for the loading state

---

## Checklist

- [ ] Users list loads and displays correctly
- [ ] Each user card shows name, email, city
- [ ] Clicking "View Details" navigates to `/users/:id`
- [ ] Detail page shows the correct user's full info
- [ ] "Back to list" navigates back
- [ ] Loading state shows while data is fetching
- [ ] No errors in the console

---

**Next step:** Go to `04-validation.md`.
