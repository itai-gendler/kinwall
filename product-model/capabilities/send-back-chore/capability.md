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

# Send a chore back

Say Not yet to a tick waiting for a parent's OK, with an optional note the kid sees.
