# Tag System

## Scope

- Color-coded labels for tags.
- Many-to-many relationship between todos and tags.
- Full tag management CRUD.
- Filtering by tag.

## Functional Requirements

1. Tags have a name and color.
2. Users can create, read, update, and delete tags.
3. A todo can hold multiple tags, and a tag can belong to multiple todos.
4. Users can assign/unassign tags from todos.
5. Users can filter todo lists by one or more tags.

## Validation

- Tag names must be non-empty after trimming.
- Duplicate tag names should be prevented (case-insensitive normalization recommended).
- Color values must follow an accepted format (e.g., hex).
