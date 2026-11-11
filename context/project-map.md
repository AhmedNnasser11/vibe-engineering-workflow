# Project Map

Small, always-loaded map of the repo. Update it with `/update-context` whenever paths change. Keep it under ~150 lines.

| Path | What lives there |
|---|---|
| `apps/web/` | Next.js storefront + admin (App Router) |
| `apps/api/` | NestJS API |
| `packages/ui/` | Shared UI components (shadcn-based, do not edit generated primitives) |
| `packages/types/` | Shared types and schemas |
| `context/` | Agent context, loaded on demand |
| `prompts/` | Plans (`T-XXX-*.md`); finished ones in `prompts/completed/` |
| `decisions/` | Approved ADRs |

## Feature index

| Feature | Web | API | Plan |
|---|---|---|---|
| Products | `apps/web/src/features/products/` | `apps/api/src/products/` | T-001 |
