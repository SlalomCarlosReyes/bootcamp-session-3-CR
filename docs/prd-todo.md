# Product Requirements Document (PRD) - TODO App Upgrade

## 1. Overview

We are upgrading the existing TODO app so users can organize work with due dates, priorities, and date-based filters while keeping the product simple enough for a teachable MVP. The MVP must stay lean: no backend changes, no external storage, and only the minimum data model and UI behavior needed to support local task planning.

---

## 2. MVP Scope

- Add an optional `dueDate` field to each task.
- Store `dueDate` in ISO `YYYY-MM-DD` format.
- Treat invalid `dueDate` values as absent rather than blocking task usage.
- Add a `priority` field with allowed values `P1`, `P2`, and `P3`.
- Default `priority` to `P3` when the user does not choose a value.
- Require `title` for every task.
- Add task filters for `All`, `Today`, and `Overdue`.
- Show completed tasks in the `All` view.
- Hide completed tasks in the `Today` and `Overdue` views.
- Keep task storage local only.
- Do not introduce backend or external storage changes as part of MVP.

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks so they stand out in the list.
- Add task sorting with this order: overdue tasks first, then priority from `P1` to `P3`, then due date ascending, with tasks that have no due date shown last.

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user support
- Keyboard navigation enhancements
- External storage