---
name: typescript-strict
description: Write and review strict TypeScript with no type-erasure shortcuts, checked against the installed compiler version.
---

# Strict TypeScript

## Forbidden

`any` · `unknown` used as an escape hatch · `as unknown as T` · `@ts-ignore` · `@ts-expect-error` without an issue link · `!` on external data.

## Instead

- Validate external data at the boundary with a schema, then use the inferred type.
- Use discriminated unions and narrowing instead of casts.
- Use `satisfies` to check object shapes without widening.

## Version check

Before using newer syntax, read the installed TypeScript version from the lockfile. Never upgrade TypeScript to use a feature; propose it as a decision.

## Verify

The installed compiler is the judge: `pnpm typecheck`. An editor or LSP saying "fine" is not verification.
