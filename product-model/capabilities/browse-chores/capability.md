---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: web/src/Chores.tsx#Chores
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#dueOnDate
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Browse chores

See a day's chores: one column per family member plus Anyone, each with a progress ring, today's points and the chores left, for any day from 4 days back to 9 days ahead. They exist while Chores & points is on.
