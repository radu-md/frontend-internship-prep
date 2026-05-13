# Frontend Internship Prep

This repository is a beginner-friendly learning path for preparing for a **Frontend Development Internship with Angular**.

It is designed for step-by-step learning, with small theory notes, practical exercises, mini challenges, and simple validations.

The goal of this repository is not to become an advanced Angular developer quickly.
The goal is to build a strong beginner foundation and gain enough confidence for an internship interview.

---

## Who this repository is for

This repository is for a learner who:

- is at beginner level
- has low experience in frontend development
- wants to learn HTML, CSS, JavaScript, TypeScript, OOP basics, and Angular
- needs simple explanations
- learns better with small steps and repetition
- wants to prepare for internship interviews

---

## Learning approach

Each module follows the same pattern:

1. **Theory**  
   Short and simple explanations

2. **Terminology**  
   Important technical words explained in beginner language

3. **Exercises**  
   Small tasks to practice the topic

4. **Mini Challenge**  
   A slightly bigger task to combine what was learned

5. **Validation**  
   A self-check to confirm understanding

This repository uses a **micro-learning** style:
- learn a small concept
- practice it immediately
- validate it
- move to the next step

---

## How to use each module

Every file inside a module is **numbered** to show the reading order.

Example for module `01-internet-html-css`:

```
01-theory.md          ← start here: read the theory
02-terminology.md     ← learn the key words
03-exercises.md       ← practice with small tasks
04-mini-challenge.md  ← build something slightly bigger
05-validation.md      ← check your own understanding
```

**Rules:**
- Always open files in number order — do not skip ahead
- Do not move to the next module before completing `05-validation.md`
- In the validation file, answer honestly — if you cannot answer a question, go back and review
- A topic is ready when you can explain it simply, without reading notes

---

## How to get started (Git setup)

### Git basics — what you need to know first

Git is a tool that saves the history of your code. Every change you make can be saved as a "commit" so you can always go back.

**Key concepts:**

| Term | What it means |
|------|---------------|
| **repository (repo)** | A folder tracked by Git — all your files + their full history |
| **commit** | A saved snapshot of your changes with a short message describing what you did |
| **branch** | An independent line of work — lets you experiment without breaking anything |
| **clone** | Download a copy of a remote repository to your computer |
| **fork** | Your own personal copy of someone else's repository on GitHub |
| **push** | Upload your local commits to GitHub |
| **pull / fetch** | Download new changes from GitHub to your computer |
| **remote** | A link to a repository on GitHub (e.g. `origin` = your fork, `upstream` = the original) |

**The most used commands:**

```bash
git status                        # See which files changed
git add .                         # Stage all changes (ready to commit)
git add filename.md               # Stage a specific file only
git commit -m "your message"      # Save a snapshot with a description
git push                          # Upload commits to GitHub
git pull                          # Download latest changes from GitHub
git log --oneline                 # See recent commits in one line each
```

**Good commit message habits:**
```bash
git commit -m "Complete module 01 theory"      # ✅ clear and specific
git commit -m "fix"                            # ❌ too vague
git commit -m "done"                           # ❌ says nothing useful
```

---

**Step 1 — Fork this repository**

Click the **Fork** button at the top right of this page on GitHub.
This creates your own personal copy of the repository under your account.
You will do all your work in your fork — the original stays clean.

**Step 2 — Clone your fork to your computer**

```bash
git clone https://github.com/YOUR-USERNAME/frontend-internship-prep.git
cd frontend-internship-prep
```

Replace `YOUR-USERNAME` with your GitHub username.

**Step 3 — Connect to the original repository (to receive new modules)**

```bash
git remote add upstream https://github.com/radu-md/frontend-internship-prep.git
```

This lets you pull new content when the mentor adds new modules.

**Step 4 — Start working**

Open the folders in order, read the files by number, and complete the exercises.
When you finish a file or exercise, commit and push your work:

```bash
git add .
git commit -m "Complete module 01 exercises"
git push
```

**Step 5 — Get new modules from the mentor**

When the mentor adds new content, sync it to your fork:

```bash
git fetch upstream
git merge upstream/main
git push
```

---

## Study order

Follow the modules in order:

1. `01-internet-html-css`
2. `02-javascript-basics`
3. `03-javascript-dom`
4. `04-javascript-algorithms`
5. `05-typescript-oop`
6. `06-angular-basics`
7. `07-angular-next-steps`
8. `08-algorithms-easy`
9. `09-final-mini-project`
10. `interview-prep`

Do not rush.
It is better to complete each module well than to read everything quickly.

---

## Recommended study rhythm

Recommended pace:

- **5 days per week**
- **1.5 to 3 hours per day**

Suggested daily structure:

- 20–30 min theory
- 30–60 min coding practice
- 15 min terminology review
- 15–30 min exercises or validation

If needed, even **1 hour per day consistently** is enough to make good progress.

---

## Module overview

### 01 - Internet, HTML, CSS
Learn:
- what frontend development is
- how websites work
- HTML basics
- CSS basics
- page structure
- forms
- layout
- responsive design basics

### 02 - JavaScript Basics
Learn:
- variables
- data types
- arrays
- objects
- functions
- conditions
- loops
- simple problem solving

### 03 - JavaScript DOM
Learn:
- DOM basics
- events
- form handling
- changing page content with JavaScript
- simple interactive UI behavior

### 04 - JavaScript Algorithms and Common Patterns
Learn:
- sorting arrays (numbers and objects)
- searching with find, findIndex, some, every
- removing duplicates
- grouping data
- transforming data with reduce
- chaining array methods
- common string patterns

### 05 - TypeScript and OOP
Learn:
- TypeScript basics
- types
- interfaces
- classes
- objects
- constructor
- encapsulation
- inheritance
- simple OOP terminology

### 06 - Angular Basics
Learn:
- Angular project structure
- components
- templates
- interpolation
- property binding
- event binding
- two-way binding
- directives
- pipes

### 07 - Angular Next Steps
Learn:
- services
- dependency injection
- routing
- forms
- HTTP requests
- observables basics
- component communication

### 08 - Easy Algorithms
Learn:
- simple coding exercises for interview confidence
- string exercises
- array exercises
- object exercises
- basic logic building

### 09 - Final Mini Project
Build one small Angular project to practice:
- structure
- components
- forms
- service usage
- API or mock data
- presentation skills

### Interview Prep
Prepare for:
- technical terminology
- beginner JavaScript questions
- beginner Angular questions
- OOP basics
- project presentation
- internship interview communication

---

## Progress tracking

Use the file `progress-checklist.md` to track progress.

Do not move forward too fast if:
- the concepts are still confusing
- the exercises cannot be solved alone
- the terminology cannot be explained in simple words

A topic is “good enough” when it can be:
- understood
- explained simply
- used in a small exercise

---

## External learning resources

These resources are useful as support materials:

- Git: https://www.w3schools.com/git/
- OOP / Programming basics: https://www.w3schools.com/programming/index.php
- JavaScript: https://www.w3schools.com/js/default.asp
- Angular: https://www.w3schools.com/angular/default.asp

Important:
This learning path focuses on **modern Angular**, not **AngularJS**.

- **AngularJS** is the older framework, also known as Angular 1.x
- **Angular** usually means the modern framework (Angular 2+), which is what most internship and job descriptions refer to today

For this repository and interview preparation, the recommended Angular resource is:

- https://www.w3schools.com/angular/default.asp

---

## Ground rules for studying

- Learn in order
- Do not skip validation
- Do not copy code without understanding it
- Try to explain each topic aloud
- Rebuild small examples from memory
- Focus on consistency, not speed
- Ask questions when something is unclear

---

## Main goal

By the end of this learning path, the learner should be able to:

- build simple responsive pages
- write basic JavaScript code
- understand beginner TypeScript and OOP concepts
- build a small Angular application
- solve easy coding problems
- explain basic frontend terminology
- present a small project in an internship interview

---

## Final note

This repository is built for progress in **small steps**.

The priority is:
**clarity -> practice -> confidence**

Not perfection.

Keep going one module at a time.
