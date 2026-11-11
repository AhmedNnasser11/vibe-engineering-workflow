---
name: responsive-ui
description: Plan and build UI that works as a real mobile experience, plus tablet, desktop, RTL/LTR, accessibility, and theme tokens.
---

# Responsive UI

Read `context/ui-context.md` and `context/responsive-ui.md` first.

## Non-negotiable

Mobile is not a shrunken desktop. For every UI change, state the behavior for: desktop, tablet, mobile, RTL, LTR, keyboard/screen reader, light/dark tokens.

## Component split rule

- Only layout differs → one component, responsive classes.
- Interaction differs (table vs. cards, dialog vs. bottom sheet, sidebar vs. tab bar) → separate presentation components.
- Business logic, hooks, schemas, services, types → always shared.

## RTL

Use logical properties (`ms-`, `me-`, `start`, `end`), never `left`/`right`. Flip directional icons. Test both directions.
