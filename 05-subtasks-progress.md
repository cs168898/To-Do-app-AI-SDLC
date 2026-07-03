# Subtasks & Progress Tracking

## Scope

- Checklist-style subtasks.
- Visual progress bars for completion percentage.
- Explicit position/order management for subtasks.
- Cascade delete behavior.

## Functional Requirements

1. A todo can have zero or more subtasks.
2. Subtask fields include text, completion state, and position.
3. Users can add, edit, complete, uncomplete, reorder, and delete subtasks.
4. Progress is calculated as:
   - `0%` when no subtasks
   - otherwise `(completed / total) * 100`
5. Progress UI updates immediately on subtask state changes.

## Data Integrity

- Position values remain deterministic after insert/reorder/delete.
- Deleting a parent todo deletes all child subtasks.
