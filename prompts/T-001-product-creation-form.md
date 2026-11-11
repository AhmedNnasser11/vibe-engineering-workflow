# T-001: Product creation form

Status: draft  ← example output of `/plan-feature Product creation form`

## Goal
Store owner can create a product (name AR/EN, price, stock, images) from the admin.

## Context Read
- `context/project-map.md`, `context/ui-context.md`, `context/responsive-ui.md`, `context/api-conventions.md`
- skills: `vibe-planning`, `responsive-ui`, `typescript-strict`

## Existing Code Inspected
- `apps/api/src/products/products.controller.ts` — has `GET` only
- `packages/types/src/product.ts` — `ProductSchema` exists, no create schema

## Assumptions
- Images upload to existing storage service; this task only stores URLs.
- Price stored as integer minor units.

## Decisions Requiring Approval
1. Separate mobile form (stepper) vs. one long form? Proposed: stepper on mobile, single page on desktop.
2. Is SKU required in MVP? Proposed: optional.

## Files To Create
- `packages/types/src/product-create.ts`
- `apps/web/src/features/products/create/ProductCreateForm.tsx`
- `apps/web/src/features/products/create/ProductCreateStepper.mobile.tsx`
- `apps/web/src/features/products/create/useProductCreate.ts`

## Files To Modify
- `apps/api/src/products/products.controller.ts` — add `POST /products`
- `apps/api/src/products/products.service.ts` — `create()` scoped by `tenantId`

## UI
- Desktop: two-column form, sticky save bar.
- Tablet: single column.
- Mobile: 3-step stepper, bottom primary button.
- RTL/LTR: logical spacing; AR name field first in RTL.
- A11y: labels, error summary focused on submit.

## Security / API
- Auth: store-admin role. Tenant from session, never from body.
- Body validated with `ProductCreateSchema`.

## Acceptance Criteria
- [ ] Valid submit creates a product visible in the list.
- [ ] Invalid price shows a field error in both locales.
- [ ] Request with another tenant's id in body still writes to the session tenant.

## Verification Commands
- `pnpm typecheck`
- `pnpm lint`
- `pnpm test --filter api -- products`

## Out Of Scope
Variants, categories, bulk import.
