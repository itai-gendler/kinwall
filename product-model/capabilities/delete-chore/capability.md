---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Delete a chore

Delete a chore from every list. A chore that was ever done is archived instead, so its points and history stay.
