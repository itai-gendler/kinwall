---
appliesTo:
- type: entity
  id: family-member
  effect: changes
  facts:
  - Reward goal
permits:
- actors:
  - parent
- actors:
  - wall-screen
- related:
  - verb: is
    entity: kid
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# A reward goal is set by a parent, at a wall screen, or on the person's own device

A kid's own device sets only that kid's goal; a wall screen and a parent's device set anyone's.
