# Export & Import

## Scope

- JSON-based backup and restore.
- ID remapping on import.
- Relationship preservation (subtasks, tags, recurrence links, etc.).
- Strong validation during import.

## Functional Requirements

1. Export includes todos and all related entities in a JSON document.
2. Import accepts valid JSON backups and reconstructs application state.
3. Imported IDs are remapped to avoid collisions with existing records.
4. Relationship references are rewritten using the new IDs.

## Validation & Safety

- Reject invalid JSON and schema-incompatible payloads.
- Validate required fields before writing data.
- Import should be transactional where possible to avoid partial restores.
