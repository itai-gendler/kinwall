---
appliesTo:
- type: entity
  id: chore-idea
  effect: changes
  to: Not this time
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents decline chore ideas

Saying Not this time is for parents' devices.
