# Architecture

- Monorepo: `apps/*` depend on `packages/*`, never on each other.
- Web calls API through a BFF route; the browser never holds API secrets.
- Every DB query is scoped by `tenantId`.
- Validation at the boundary with shared schemas from `packages/types`.
