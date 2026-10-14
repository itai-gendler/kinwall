---
appliesTo:
- type: entity
  id: list
  effect: changes
  from: Archived
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
---

# Only parents restore lists

Restoring is for parents' devices.
