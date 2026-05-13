# Module 06 — Mini Challenge: Angular Basics

---

## Challenge: User profile page

**Goal:** Build a small Angular app with a user profile component that uses all the binding types from this module.

---

## What to build

A single-page Angular app with a `UserProfileComponent` that displays:

### Profile card
- Avatar image (use any image URL or `https://i.pravatar.cc/150`)
- Full name
- Job title
- A short bio (text)
- Online/offline status badge

### Stats section
Using `*ngFor`, display a list of skills:
```ts
skills = ['HTML', 'CSS', 'JavaScript', 'TypeScript', 'Angular'];
```

### Edit mode
- A button "Edit Profile" that toggles a simple edit form
- The form shows when `isEditing` is true (use `*ngIf`)
- The form has a text input for the name, bound with `[(ngModel)]`
- The profile card updates in real time as the user types
- A button "Save" that sets `isEditing` back to false

---

## Requirements

- Use **interpolation** to display name, title, bio
- Use **property binding** for the avatar `src`
- Use **event binding** for the buttons
- Use **two-way binding** for the name input
- Use `*ngFor` for the skills list
- Use `*ngIf` for the edit form

---

## Checklist

- [ ] Profile card shows all information
- [ ] Skills are displayed as a list using `*ngFor`
- [ ] "Edit Profile" button shows the form
- [ ] Typing in the name input updates the displayed name live
- [ ] "Save" button hides the form
- [ ] No errors in the console

---

**Next step:** Go to `05-validation.md`.
