---
status: pending
title: Minimal personal todo app with due dates
---

1. Add a shared type in `src/types/todo.ts` describing a task: id, title, done flag, optional due date, created time. Outcome: one consistent shape across the app.
2. Create `src/hooks/useTodos.ts` to manage tasks (add, toggle, edit, delete, clear completed) and persist them in the browser's local storage. Outcome: tasks survive page reloads, no account needed.
3. Create `src/lib/dates.ts` with helpers to format due dates ("Today", "Tomorrow", "Mar 5") and detect overdue tasks. Outcome: friendly date labels, overdue ones flagged.
4. Build components in `src/components/`:
   - `TodoForm.tsx`: text input plus optional date picker and Add button.
   - `TodoItem.tsx`: checkbox, title (strikethrough when done), due-date label (red when overdue), inline edit, delete button.
   - `TodoList.tsx`: renders items, sorted with unfinished first then by due date, with a friendly empty state.
   - `TodoFooter.tsx`: "N tasks left", All / Active / Completed filter tabs, and Clear completed.
   Outcome: a complete add, complete, edit and delete flow.
5. Replace the placeholder in `src/routes/index.tsx` with the todo page: a centered card, heading with today's date, form, list and footer. Outcome: the home page is the working app.
6. Style with Tailwind for a minimal, clean look: white/neutral background, a single soft accent color, generous spacing, subtle borders, responsive on mobile. Keep `src/styles/global.css` starting with the Tailwind import and set a clean system font there.
7. Verify: adding, completing, editing, deleting, filtering, overdue highlighting and reload persistence all work.
