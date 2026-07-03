# Recurring Todos

## Scope

- Support recurrence patterns: daily, weekly, monthly, yearly.
- Automatically create the next instance when a recurring todo is completed.
- Correctly calculate next due dates.
- Inherit metadata to newly created instances.

## Functional Requirements

1. Recurrence values are: `daily`, `weekly`, `monthly`, `yearly`.
2. Completion of a recurring instance creates the next pending instance.
3. Next due date logic:
   - Daily: +1 day
   - Weekly: +7 days
   - Monthly: same day-of-month when possible, otherwise month-end fallback
   - Yearly: same month/day with leap-year handling
4. New instance inherits title, description, priority, tags, reminders, and subtasks template metadata.
5. Parent linkage/series metadata must be preserved for traceability.

## Guardrails

- Ensure only one next instance is created per completion event.
- Use Singapore timezone for recurrence boundaries.
