---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ChoreEditSheet
---

# Edit a chore

Change a chore's title, emoji, points, who it is for, its repeat, start time, timer, checklist or whether it needs a parent's OK. Points already earned stay as they were.
