---
appliesTo:
- type: entity
  id: chore-completion
  effect: changes
  to: Not yet
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

# Only parents send chores back

Saying Not yet is for parents' devices.
