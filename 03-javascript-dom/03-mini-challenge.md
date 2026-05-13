# Module 03 — Mini Challenge: JavaScript DOM

This task combines DOM manipulation, events, localStorage, and basic logic.

---

## Challenge: Notes App

**Goal:** Build a simple notes app where the user can add, view, and delete notes. Notes are saved to `localStorage` so they survive a page refresh.

---

## Features to build

1. **Add a note**
   - A text input and an "Add Note" button
   - When clicked, the note is added to the list
   - Input is cleared after adding
   - Empty input should not add a note

2. **Display notes**
   - Notes appear as a list on the page
   - Each note shows the text and a "Delete" button

3. **Delete a note**
   - Clicking "Delete" removes that note from the list

4. **Persist with localStorage**
   - Notes are saved to `localStorage` on every change
   - When the page loads, existing notes are loaded and displayed

---

## HTML starter

```html
<!DOCTYPE html>
<html>
<head>
  <title>Notes App</title>
  <style>
    /* add your styles */
  </style>
</head>
<body>
  <h1>My Notes</h1>

  <input type="text" id="note-input" placeholder="Write a note..." />
  <button id="add-btn">Add Note</button>

  <ul id="notes-list"></ul>

  <script>
    // your JavaScript here
  </script>
</body>
</html>
```

---

## Steps to solve

1. Load notes from `localStorage` on startup (parse JSON — it is an array)
2. Write a `renderNotes()` function that clears the list and redraws it from the array
3. "Add Note" button:
   - Read the input value
   - If not empty, push to the array
   - Save to `localStorage`
   - Call `renderNotes()`
4. "Delete" button for each note:
   - Remove the item from the array by index
   - Save to `localStorage`
   - Call `renderNotes()`

---

## Checklist before finishing

- [ ] Adding a note shows it in the list
- [ ] Empty input is ignored
- [ ] Delete button removes the correct note
- [ ] Refreshing the page keeps the notes
- [ ] No errors in the browser console

---

**Next step:** Go to `04-validation.md`.
