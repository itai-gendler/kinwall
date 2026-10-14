---
actors:
- kid
references:
- kind: code
  role: implementation
  target: web/src/GetStuffDone.tsx#GetStuffDone
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Finish a checklist chore

## Goal

A kid gets a routine chore, such as Bedtime, done by working through its checklist.

## Success criterion

Every checklist item for the kid is ticked and the chore is done or waiting for a parent's OK.
