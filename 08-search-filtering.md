# Search & Filtering

## Scope

- Real-time text search.
- Advanced search over title and tags.
- Multi-criteria filters.
- Efficient client-side behavior.

## Functional Requirements

1. Search updates results as the user types.
2. Search matches todo title and associated tags.
3. Filters can be combined (e.g., priority + tag + completion + date range).
4. Empty query returns unfiltered baseline list.

## Performance Expectations

- Debounce user input to avoid unnecessary recomputation.
- Keep filtering/search logic responsive for typical list sizes.
- Preserve stable ordering when applying/removing filters.
