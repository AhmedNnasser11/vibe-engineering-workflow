# API Conventions

- Errors: `{ code, message, details? }` with stable `code` strings.
- Pagination: cursor-based, `{ items, nextCursor }`.
- Contract changes require `/update-context` and, if breaking, an ADR.
