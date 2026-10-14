---
availability:
- place: web-app::family
domain: rewards
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ApprovalQueue
---

# Approve a reward request

Approve a reward request waiting for a parent's OK, from Reward requests or To approve on Chores. For a split, the others' shares come off then.
