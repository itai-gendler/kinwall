---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#choreRepeatError
- kind: code
  role: implementation
  target: server/src/recurrence.ts#isValidRrule
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ChoreEditSheet
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Add a chore

Add a one-off or repeating chore for one family member or anyone, with points and optionally a start time, timer, checklist and whether it needs a parent's OK. They exist while Chores & points is on.
