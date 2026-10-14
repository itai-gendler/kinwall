---
appliesTo:
- type: entity
  id: list
  effect: changes
  to: Archived
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
---

# Only parents archive lists

Archiving is for parents' devices.
