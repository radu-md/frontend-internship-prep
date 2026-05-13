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
04-javascript-algorithms/
05-typescript-oop/
06-angular-basics/
07-angular-next-steps/
08-algorithms-easy/
09-final-mini-project/
interview-prep/
progress-checklist.md
```

The `interview-prep/` folder contains:

- `01-common-questions.md`
- `02-javascript-questions.md`
- `03-angular-questions.md`
- `04-hr-questions.md`

---

## Module content conventions

Every module follows the **same internal structure**. When adding content to any module, create these files:

| File | Purpose |
| ------------------- | ------------------------------------------------------------------------ |
| `01-theory.md`         | Short plain-language explanation of the concept with minimal examples    |
| `02-terminology.md`    | Glossary — one term, one simple explanation, one tiny example            |
| `03-exercises.md`      | Small focused tasks: fill-in-code, modify examples, write tiny functions |
| `04-mini-challenge.md` | One slightly bigger task combining concepts from the module              |
| `05-validation.md`     | Self-check questions the learner answers themselves                      |

Files are numbered so the learner always knows what to open next. Always follow the `01-` → `05-` order when creating new files. Each file should be completable in **10–30 minutes**.

Modules without a terminology file skip `02-terminology.md` and renumber the rest:
- `03-javascript-dom`: `01-theory` → `02-exercises` → `03-mini-challenge` → `04-validation`
- `07-angular-next-steps`: `01-theory` → `02-exercises` → `03-mini-challenge` → `04-validation`
- `08-algorithms-easy`: `01-theory` → `02-exercises` → `03-solutions` → `04-validation`

The `05-typescript-oop/` module uses `02-oop-cheatsheet.md` instead of `02-terminology.md`.  
The `09-final-mini-project/` module uses `01-brief.md`, `02-steps.md`, `03-checklist.md`, `04-presentation-guide.md`.

---

## 9-week learning rhythm

| Week | Module                          | Focus                                                              |
| ---- | ------------------------------- | ------------------------------------------------------------------ |
| 1    | `01-internet-html-css`          | What frontend is, HTML, CSS, layout, responsive basics             |
| 2    | `02-javascript-basics`          | Variables, arrays, objects, functions, loops, DOM basics           |
| 3    | `03-javascript-dom`             | Deeper JS, async/await, localStorage, beginner problem solving     |
| 4    | `04-javascript-algorithms`      | Sorting, searching, grouping, reduce, chaining — practical patterns |
| 5    | `05-typescript-oop`             | TypeScript basics, OOP vocabulary for interviews                   |
| 6    | `06-angular-basics`             | Components, templates, directives, pipes, CLI                      |
| 7    | `07-angular-next-steps`         | Services, routing, forms, HTTP, @Input/@Output                     |
| 8    | `08-algorithms-easy` + `09-final-mini-project` | Interview algorithm prep + build final project    |
| 9    | `interview-prep` + Revision     | Mock interviews, project presentation, terminology review          |

`04-javascript-algorithms` covers **practical JS patterns** used in real code (sort, search, reduce, chaining).
`08-algorithms-easy` covers **interview puzzle problems** (palindrome, FizzBuzz, reverse string).
These two modules are complementary, not redundant.

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
