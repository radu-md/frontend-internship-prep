# Copilot Instructions

## Context

This repository is a structured micro-learning path created to prepare juniors for a **Frontend Development Internship with Angular**.

- The learner is a **complete beginner** with very low frontend experience and no prior knowledge of algorithms, OOP, or technical terminology
- The mentor reviews, adds content, and tracks progress
- The learner studies independently by following the modules in order
- This is **not** a deployable application — it is an educational resource made of markdown files and small code exercises

The goal is **not** to become an advanced Angular developer fast. The goal is:

1. Build a solid beginner foundation
2. Gain enough confidence to succeed in an internship interview
3. Be able to explain and demonstrate one small project clearly

---

## Repository structure

Modules must be studied strictly in order:

```
01-internet-html-css/
02-javascript-basics/
03-javascript-dom/
04-typescript-oop/
05-angular-basics/
06-angular-next-steps/
07-algorithms-easy/
08-final-mini-project/
interview-prep/
progress-checklist.md
```

The `interview-prep/` folder contains:

- `common-questions.md`
- `hr-questions.md`
- `angular-questions.md`
- `javascript-questions.md`

---

## Module content conventions

Every module follows the **same internal structure**. When adding content to any module, create these files:

| File                | Purpose                                                                  |
| ------------------- | ------------------------------------------------------------------------ |
| `theory.md`         | Short plain-language explanation of the concept with minimal examples    |
| `terminology.md`    | Glossary — one term, one simple explanation, one tiny example            |
| `exercises.md`      | Small focused tasks: fill-in-code, modify examples, write tiny functions |
| `mini-challenge.md` | One slightly bigger task combining concepts from the module              |
| `validation.md`     | Self-check questions the learner answers themselves                      |

Each file should be completable in **10–30 minutes**. Prefer many short files over one long file.

The `04-typescript-oop/` module uses `oop-cheatsheet.md` instead of `terminology.md`.  
The `08-final-mini-project/` module uses `brief.md`, `steps.md`, `checklist.md`, `presentation-guide.md`.

---

## 8-week learning rhythm

| Week | Module                          | Focus                                                        |
| ---- | ------------------------------- | ------------------------------------------------------------ |
| 1    | `01-internet-html-css`          | What frontend is, HTML, CSS, layout, responsive basics       |
| 2    | `02-javascript-basics`          | Variables, arrays, objects, functions, loops, DOM basics     |
| 3    | `03-javascript-dom`             | Deeper JS, async/await, localStorage, simple algorithms      |
| 4    | `04-typescript-oop`             | TypeScript basics, OOP vocabulary for interviews             |
| 5    | `05-angular-basics`             | Components, templates, directives, pipes, CLI                |
| 6    | `06-angular-next-steps`         | Services, routing, forms, HTTP, @Input/@Output               |
| 7    | `interview-prep` + mini project | Convert learning into interview answers, build final project |
| 8    | Revision                        | Mock interviews, algorithm review, project presentation      |

Algorithms appear in **Week 3** (not earlier) — the learner needs UI/JS confidence first.

---

## Final project guidance

The recommended final projects (in priority order):

1. **Task Manager** — components, service, routing, form, local state
2. **Movie Search App** — components, service, HTTP call, routing

The project should cover: components, routing, a service, an API call or mock data, and a form. It must be presentable in 2–3 minutes in an interview.

---

## Writing style for all content

- Use **simple, short sentences** — assume zero prior experience
- Define every technical term before using it
- Prefer concrete examples over abstract explanations
- Pair every new concept with a minimal code snippet
- Exercises must state their goal clearly at the top (e.g., "Write a function that returns the largest number in an array.")
- Validation files must be phrased as self-check questions: "Can you explain X?", "Can you write X from memory?"
- Encourage the learner: the tone should be supportive and confidence-building

---

## Code examples

- HTML/CSS: minimal, self-contained — no frameworks, no build tools
- JavaScript/TypeScript: vanilla only, no external dependencies unless the module specifically introduces a library
- Angular: **modern Angular (Angular 2+) only** — never reference AngularJS / Angular 1.x
- Keep examples short enough to understand in one reading
- Always use explicit, readable code — never clever shortcuts or idiomatic one-liners

---

## Topics explicitly out of scope

Do **not** include content on these topics — they are too advanced for this learning path:

- Advanced RxJS operators
- NgRx or state management libraries
- Advanced Angular performance optimization
- System design
- Advanced algorithms or competitive programming
- Advanced design patterns
- Heavy backend/server concepts

OOP coverage should be **minimal**: enough to answer basic interview questions about classes, inheritance, encapsulation, and interfaces — nothing more.

---

## What this repository is NOT

- Not a deployable app (no `package.json` at root, no build pipeline)
- Not a comprehensive Angular reference
- Not for intermediate or advanced developers
