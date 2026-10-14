---
appliesTo:
- type: entity
  id: chore-completion
  effect: changes
  to: Done
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

# Only parents approve chores

Approving a tick waiting for an OK is for parents' devices.
