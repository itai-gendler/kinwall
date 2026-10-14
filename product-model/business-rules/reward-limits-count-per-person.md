---
appliesTo:
- type: capability
  id: redeem-reward
- type: entity
  id: reward
  facts:
  - Limit
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
---

# A reward's limit counts each person's requests in the current day or week, except declined ones

Days and weeks follow the family's timezone and first day of the week; a split counts for the person who asked.
