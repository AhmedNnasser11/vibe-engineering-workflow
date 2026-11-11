---
description: Run and interpret the verification checks for a scope. Does not fix anything.
agent: build
---

Verify: $ARGUMENTS

Run, scoped to the affected packages where possible:
1. `pnpm typecheck`
2. `pnpm lint`
3. relevant tests

For each: command, pass/fail, the key error lines. If something fails, say whether it is caused by this task or pre-existing. Do not fix; propose next steps.
