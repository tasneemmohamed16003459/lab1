# Todo App - Full Stack Filtering Implementation

I completed the task by adding end-to-end filtering functionality, allowing users to switch between viewing **All**, **Active**, and **Done** tasks.


## What Was Completed


### 1. In (`controllers/todoController.js`)
* Updated the `getTodos` controller to inspect incoming query parameters (`req.query.done`).
* Built dynamic database filtering: passing `?done=true` queries completed tasks, `?done=false` queries active tasks, and omitting the parameter returns all tasks.
* Aligned the Mongoose query filter to match the schema's field name (`done`).

### 2. In (`api/todos.js`)
* Refactored `fetchTodos` to accept an optional status filter.
* Used Axios parameters (`params: { done: filter }`) to automatically format query strings when making request calls to the server.

### 3. In (`App.jsx`)
* Added React `filter` state (`'all'`, `'active'`, `'done'`).
* Integrated interactive filter buttons into the receipt UI layout, giving visual feedback for the currently active view.
* Made `useEffect` automatically trigger data re-fetching whenever a user clicks a different tab filter.

* <img width="1436" height="853" alt="Screenshot 2026-09-14 at 7 20 56 PM" src="https://github.com/user-attachments/assets/be9a851a-e83a-4412-ad37-8444bd18c30f" />
