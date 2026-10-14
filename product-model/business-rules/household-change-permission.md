---
appliesTo:
- type: entity
  id: household
  effect: changes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/settings.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents change the family's settings

The family name, timezone, features, chore and calendar settings are changed from parent devices; a wall screen or kid's device keeps only its own look.
