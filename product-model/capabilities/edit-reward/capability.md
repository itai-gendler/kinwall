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

# Edit a reward

Change a reward's name, emoji, cost, who it is for, whether it needs an OK, or its limit. Past requests keep what they were.
