# Module 09 — Project Steps: Task Manager

Follow these steps in order. Build and test each step before moving to the next.

---

## Step 1 — Create the project

```bash
ng new task-manager
cd task-manager
ng serve
```

Open `http://localhost:4200` and confirm the default page loads.

---

## Step 2 — Create the Task interface

Create a file `src/app/models/task.model.ts`:

```ts
export interface Task {
  id: number;
  title: string;
  status: 'pending' | 'done';
  createdAt: Date;
}
```

---

## Step 3 — Create the TaskService

```bash
ng generate service services/task
```

In `task.service.ts`:
- Add a private `tasks: Task[]` array with 2–3 starter tasks
- Add methods:
  - `getTasks(): Task[]` — returns all tasks
  - `addTask(title: string): void` — creates a new task and adds it
  - `toggleTask(id: number): void` — switches status between pending/done
  - `deleteTask(id: number): void` — removes the task

---

## Step 4 — Create the TaskItem component

```bash
ng generate component task-item
```

- Add `@Input() task: Task`
- Add `@Output() deleted = new EventEmitter<number>()`
- Add `@Output() toggled = new EventEmitter<number>()`
- Template: show title, status, a "Done/Undo" button, a "Delete" button
- Buttons emit the events with the task id

---

## Step 5 — Create the TaskList component

```bash
ng generate component task-list
```

- Inject `TaskService`
- Load tasks in `ngOnInit`
- Add a `filter: 'all' | 'pending' | 'done'` property (default: `'all'`)
- Add a `filteredTasks` getter that returns tasks based on the filter
- Template:
  - 3 filter buttons (All / Pending / Done)
  - Use `*ngFor` to render `<app-task-item>` for each filtered task
  - Handle `(deleted)` and `(toggled)` events from TaskItem

---

## Step 6 — Create the TaskForm component

```bash
ng generate component task-form
```

- Import `ReactiveFormsModule`
- Create a form group with one field: `title` (required, minLength 3)
- Template: text input + "Add Task" button (disabled when form is invalid)
- On submit: call `taskService.addTask(title)`, reset the form

---

## Step 7 — Wire everything together in AppComponent

In `app.component.html`:

```html
<h1>Task Manager</h1>
<app-task-form></app-task-form>
<app-task-list></app-task-list>
```

Make sure all components are declared and imports are correct.

---

## Step 8 — Add basic styling

Add CSS to make the app presentable:
- Cards for each task
- Color difference for done tasks (e.g., lighter color, line-through text)
- Filter buttons that look clickable
- Form with proper input styling

---

## Step 9 — Test everything

Go through the checklist in `03-checklist.md` before considering the project done.

---

## Step 10 — Practice your presentation

Go to `04-presentation-guide.md` and practice explaining the project out loud.
