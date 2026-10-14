---
appliesTo:
- type: entity
  id: chore
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents delete chores

Wall screens and kids' devices tick chores off and undo ticks; adding, editing and deleting chores is for parent devices.
