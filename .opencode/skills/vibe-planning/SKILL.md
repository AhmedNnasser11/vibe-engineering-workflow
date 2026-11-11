---
name: vibe-planning
description: Write a reviewable implementation plan before any non-trivial change. Use for features, refactors, and anything touching more than one file.
---

# Vibe Planning

A plan is a contract between the human and the implementing agent. A fresh session with no chat history must be able to execute it.

## Template

```md
# T-XXX: <title>

Status: draft | approved | done

## Goal
## Context Read            (files and skills you loaded)
## Existing Code Inspected (files you opened, what you found)
## Assumptions
## Decisions Requiring Approval
## Files To Create
## Files To Modify
## Implementation Steps
## UI: Desktop / Tablet / Mobile / RTL-LTR / A11y   (UI tasks only)
## Security / API                                    (backend tasks only)
## Acceptance Criteria
## Verification Commands
## Out Of Scope
```

Omit sections that do not apply. Never omit Assumptions, Files, Acceptance Criteria, or Verification.

## Rules

- Every file path must exist (modify) or have an existing parent folder (create).
- Acceptance criteria are checkable statements, not intentions.
- If a decision is not yours (scope, contract, dependency, architecture), put it under "Decisions Requiring Approval" and do not assume an answer.
