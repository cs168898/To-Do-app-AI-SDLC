# Priority System

## Scope

- Three-level priority: High, Medium, Low.
- Color-coded priority badges.
- Automatic sorting by priority.
- Priority-based filtering.

## Functional Requirements

1. Priority defaults to `Medium` when omitted.
2. Accepted values are strictly `High`, `Medium`, `Low`.
3. Priority badge colors must be visually distinct and consistent across views.
4. Lists sort by priority order: `High` > `Medium` > `Low`, then stable by creation/update time.
5. Users can filter todos by one or more priority levels.

## Validation

- Reject unknown priority values.
- Preserve existing priority on partial updates when priority is not supplied.
