# Todo CRUD Operations

## Scope

- Create, read, update, and delete todo items.
- Handle all user-facing date/time values in `Asia/Singapore`.
- Apply validation rules with clear error handling.
- Support optimistic UI updates for write operations.

## Functional Requirements

1. **Create**
   - A user can create a todo with title, optional description, optional due date, and optional metadata.
   - Title is required and cannot be empty after trimming.
2. **Read**
   - Users can list all todos and view one todo by ID.
3. **Update**
   - Users can edit todo fields and completion status.
4. **Delete**
   - Users can remove a todo by ID.

## Validation & Errors

- Reject invalid payloads with deterministic error messages.
- Reject malformed dates and timezone-unsafe datetime values.
- Return not-found errors for unknown IDs.
- Prevent silent failures for create/update/delete actions.

## Timezone Rules

- Store canonical timestamps consistently and render using Singapore timezone.
- Date calculations (due labels, overdue state) must use `Asia/Singapore`.

## Optimistic UI Rules

- UI updates immediately after user action.
- Revert optimistic changes when the server/database action fails.
- Prevent duplicate optimistic inserts during retries.
