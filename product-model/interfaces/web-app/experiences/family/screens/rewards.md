---
entities:
- entity: reward
  shows:
  - Name
  - Emoji
  - Points
  - For
  - Needs a parent's OK
  - Limit
  collects:
  - Name
  - Emoji
  - Points
  - For
  - Needs a parent's OK
  - Limit
- entity: reward-request
  shows:
  - Points
  - Shares
  - Note
  - Requested
  collects:
  - Shares
  - Note
- entity: family-member
  shows:
  - Name
  - Points to spend
  - Reward goal
entryPoints:
- web-app: /#/rewards
references:
- kind: code
  role: implementation
  target: web/src/Rewards.tsx#Rewards
---

# Rewards

One person's points to spend, goal, rewards and requests, and on a parent's device the reward requests and Manage rewards.
