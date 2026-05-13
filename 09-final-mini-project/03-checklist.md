# Module 09 — Project Checklist: Task Manager

Go through each item. Only move on when everything is checked.

---

## Functionality

- [ ] App runs without errors (`ng serve` works, no console errors)
- [ ] Default tasks appear on load
- [ ] New task can be added using the form
- [ ] Form with empty input does not add a task
- [ ] Form is cleared after adding a task
- [ ] "Done/Undo" button toggles the task status
- [ ] Done tasks look visually different (e.g., line-through, different color)
- [ ] "Delete" button removes the task from the list
- [ ] Filter "All" shows all tasks
- [ ] Filter "Pending" shows only pending tasks
- [ ] Filter "Done" shows only completed tasks

---

## Code quality

- [ ] `Task` interface is defined and used everywhere
- [ ] All task logic (add, toggle, delete) is in `TaskService`
- [ ] `TaskItem` component uses `@Input` and `@Output` correctly
- [ ] `TaskList` handles the events from `TaskItem`
- [ ] The form uses `ReactiveFormsModule` with validation
- [ ] No logic is duplicated across components

---

## Appearance

- [ ] The page has a clear title
- [ ] Tasks are displayed as cards or list items
- [ ] Done and pending tasks are visually distinguishable
- [ ] Filter buttons are visible and clickable
- [ ] The form is styled and easy to use
- [ ] The app looks usable (not just default browser styles)

---

## Ready for interview?

- [ ] I can explain what each component does
- [ ] I can explain how data flows from TaskService → TaskList → TaskItem
- [ ] I can explain why I used a service instead of storing data in the component
- [ ] I can explain how `@Input` and `@Output` work with an example from this project
- [ ] I can explain how the reactive form validation works
- [ ] I can run the project from scratch and show it working

---

**Next step:** Go to `04-presentation-guide.md`.
