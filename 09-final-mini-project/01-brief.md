# Module 09 — Project Brief: Task Manager

## What you will build

A **Task Manager** — a simple Angular application where the user can create, view, and delete tasks.

This project covers the most important Angular concepts you have learned.
It is small enough to build in a few days, and complete enough to present in an interview.

---

## What the app does

1. **View all tasks** — see a list of tasks with their title and status
2. **Add a task** — type a title and submit a form to add it to the list
3. **Mark as done** — toggle a task between "pending" and "done"
4. **Delete a task** — remove a task from the list
5. **Filter tasks** — show All / Pending / Done tasks

---

## Angular concepts this project uses

| Concept | Where |
|---|---|
| Components | TaskList, TaskItem, TaskForm |
| `*ngFor` | Display the list of tasks |
| `*ngIf` | Show/hide based on filter or empty state |
| Reactive form | Add task form |
| Service | TaskService — stores and manages tasks |
| `@Input` | TaskItem receives one task from TaskList |
| `@Output` | TaskItem emits delete/toggle events to TaskList |
| Routing | Optionally navigate to a task detail page |
| Pipes | Format date added, uppercase status badge |

---

## Tech requirements

- Angular (latest version, created with Angular CLI)
- TypeScript
- No external UI libraries (use plain CSS)
- Data stored in memory (in the service) — no backend needed

---

## Data model

```ts
interface Task {
  id: number;
  title: string;
  status: 'pending' | 'done';
  createdAt: Date;
}
```

---

## Pages / Components

```
app/
├── task-list/         ← main page, shows all tasks + filter
├── task-item/         ← single task card (@Input task, @Output events)
├── task-form/         ← add task form (reactive form)
└── services/
    └── task.service.ts ← manages the task array
```

---

**Next step:** Go to `02-steps.md` to build the project step by step.
