# Reminders & Notifications

## Scope

- Browser notification support for due reminders.
- Configurable reminder timing from 15 minutes to 1 week before due time.
- Polling-based reminder checks with duplicate prevention.
- Singapore timezone-aware reminder calculations.

## Functional Requirements

1. Users can configure reminder lead times in this range:
   - 15 minutes, 30 minutes, 1 hour, 1 day, up to 1 week before due date.
2. Polling checks upcoming reminders on a fixed interval.
3. Notification dispatch occurs once per reminder event.
4. Notification permissions are requested and handled gracefully.

## Duplicate Prevention

- Store reminder dispatch state keyed by todo ID + reminder timestamp.
- Do not re-send reminders already marked as sent.
- Handle app reloads without re-firing old reminders.

## Timezone Rules

- Reminder trigger times are computed against `Asia/Singapore`.
