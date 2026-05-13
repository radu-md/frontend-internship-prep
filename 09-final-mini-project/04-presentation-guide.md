# Module 09 — Presentation Guide: Task Manager

## How to present your project in an interview

Interviewers often say: "Tell me about a project you built."

This guide gives you a structure and practice script.

---

## The 2–3 minute structure

Use this order:

1. **What the project is** (15–20 seconds)
2. **What it does — features** (30–45 seconds)
3. **What technologies you used and why** (30–45 seconds)
4. **What you learned or found challenging** (30 seconds)
5. **Offer to show the code or demo** (10 seconds)

---

## Practice script

Read this out loud — then practice without looking.

---

> "I built a Task Manager application using Angular and TypeScript.
>
> The app lets you add tasks, mark them as done, delete them, and filter the list to show all, pending, or completed tasks.
>
> I used Angular components — a TaskList, a TaskItem, and a TaskForm. The TaskItem component receives data from the parent using @Input, and sends events back using @Output and EventEmitter. All the data and task logic — like adding and deleting — lives in a TaskService, which I injected into the components using dependency injection.
>
> For the form, I used Angular Reactive Forms with validation, so the user can't submit an empty task.
>
> The main thing I learned was how to structure an Angular app with services and component communication. At first I had all the logic in the component, but then I moved it to a service, and the code became much cleaner.
>
> I can show you the code or run it if you'd like."

---

## Key things to mention (even if not asked)

These show you understand Angular:
- Components (TaskList, TaskItem, TaskForm)
- Service (TaskService) and why you used it
- `@Input` and `@Output` between parent and child
- Reactive form with validation
- Dependency injection

---

## Common follow-up questions and how to answer

**"Why did you put the logic in a service?"**
> "So I could keep the components clean and focused only on the view. The service is the single source of truth for the task data."

**"What is the difference between @Input and @Output?"**
> "@Input is how a parent passes data down to a child component. @Output is how a child sends events back up to the parent."

**"What is dependency injection?"**
> "It's how Angular provides services to components automatically. Instead of creating a service manually, I declare it in the constructor and Angular handles the rest."

**"What was the hardest part?"**
> Be honest. Common good answers:
> - "Understanding how @Input and @Output connect the components."
> - "Getting the reactive form validation to display error messages correctly."
> - "Figuring out how to filter the list without modifying the original array."

**"What would you add if you had more time?"**
> - "I'd add localStorage to persist tasks after refresh."
> - "I'd add a backend API to save tasks to a database."
> - "I'd add a deadline field and sort by due date."

---

## Demo tips

- Have the app running before the interview
- Show: add a task, mark it done, filter, delete
- Keep it short — 60–90 seconds of demo is enough
- If something breaks, stay calm: "Let me check that quickly."

---

## Final advice

You don't need a perfect project. You need to explain it clearly.

Interviewers for junior/intern roles are looking for:
- Do you understand what you built?
- Can you explain the basic concepts?
- Are you willing to learn?

Be confident. Be honest. You have built something real.
