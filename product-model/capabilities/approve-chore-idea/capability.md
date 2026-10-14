---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ApprovalQueue
---

# Approve a chore idea

Say yes to a kid's chore idea, keeping or changing its points, days, start time or timer, with an optional note. It becomes an ordinary chore for that kid.
