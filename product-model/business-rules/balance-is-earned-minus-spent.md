---
appliesTo:
- type: capability
  id: redeem-reward
- type: capability
  id: uncomplete-chore
- type: entity
  id: family-member
  facts:
  - Points to spend
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Points to spend are everything earned minus everything spent

Chores, check-ins and bonus points add; rewards and sticker packs spend. A request a parent declines gives its points back; unticking a chore takes its points back, so a balance can fall below zero, and new purchases wait until it is back up.
