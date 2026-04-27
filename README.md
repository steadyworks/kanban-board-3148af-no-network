# Kanban Board

Build a Kanban board application using React that lets users organize cards across three columns.

## Requirements

### Board Layout

- Three columns: **Backlog**, **In Progress**, and **Done**
- Each column displays its name as a heading
- Each column shows the count of cards it currently contains in the format `"N cards"`

### Adding Cards

- An input field with `placeholder="New card title"` and an **"Add"** button at the top of the page
- New cards are always added to the **Backlog** column
- Empty titles should be ignored (no card added)

### Moving Cards

- Cards in **Backlog** have a **"→"** button that moves them to **In Progress**
- Cards in **In Progress** have a **"←"** button (move back to Backlog) and a **"→"** button (move forward to Done)
- Cards in **Done** have a **"←"** button that moves them back to **In Progress**

### Deleting Cards

- Every card has a **"Delete"** button that removes it from the board

### Persistence

- The full board state must persist in `localStorage` using the key `"kanban-board"`
- State should be fully restored on page reload

### Data Model

Each card is a JSON object:
- `id`: unique identifier (`Date.now().toString()` or similar)
- `title`: string
- `column`: `"backlog"` | `"in-progress"` | `"done"`

### Technical Details

- The React app is set up with Vite in `/app/`
- Edit `src/App.jsx` to implement the board
- Use `data-testid="column-backlog"`, `data-testid="column-in-progress"`, and `data-testid="column-done"` on the three column container elements
- Style with `src/App.css` as needed
