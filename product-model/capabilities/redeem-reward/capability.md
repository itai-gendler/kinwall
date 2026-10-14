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
  target: web/src/Rewards.tsx#SplitSheet
- kind: doc
  role: intent
  target: docs/using/rewards.md
---

# Get a reward

Spend points on a reward. The points come off at once; a request from a wall screen or kid's device waits for a parent when the reward needs an OK, and a parent's device gets it approved straight away. Several people can split a bigger reward. It exists while Chores & points and the family's Rewards setting are on.
