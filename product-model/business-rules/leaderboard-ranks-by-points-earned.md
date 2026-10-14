---
appliesTo:
- type: capability
  id: view-leaderboard
- type: entity
  id: family-member
  facts:
  - Points earned
references:
- kind: code
  role: implementation
  target: server/src/routes/leaderboard.ts
---

# The leaderboard ranks by points earned, then chores done, then name

Spending never lowers a rank; equal points and completions share a rank.
