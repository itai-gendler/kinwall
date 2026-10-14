---
appliesTo:
- type: entity
  id: chore-idea
  effect: changes
  to: Approved
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

# Only parents approve chore ideas

Ideas already waiting can still be answered after suggesting is turned off.
