---
appliesTo:
- type: capability
  id: delete-chore
- type: entity
  id: chore
  effect: changes
  to: Archived
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
---

# A chore that was ever done is archived instead of deleted

Its completions and the points earned from them stay, and it still counts on profiles and in exports.
