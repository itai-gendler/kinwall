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
  target: web/src/Rewards.tsx#RewardEditSheet
---

# Add a reward

Add a reward with a name, emoji, cost, who it is for, whether it needs a parent's OK and an optional daily or weekly limit.
