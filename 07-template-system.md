# Template System

## Scope

- Save and reuse todo templates.
- Serialize subtasks as JSON in templates.
- Calculate due dates from configurable offsets.
- Support template categories.

## Functional Requirements

1. Users can create templates from scratch or existing todos.
2. Template fields include title, description, priority, tags, subtasks JSON, and due-date offset metadata.
3. Users can apply a template to generate a new todo.
4. On apply, due date is derived from the current time plus template offset.
5. Templates can be grouped or filtered by category.

## Data Rules

- Subtasks JSON must be schema-valid before save.
- Template application must not mutate the template source data.
