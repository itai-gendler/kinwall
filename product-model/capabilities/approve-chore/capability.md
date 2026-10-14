---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ApprovalQueue
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Approve a chore

Approve a tick waiting for a parent's OK, from To approve on Chores. It earns its points as of the day it was ticked.
