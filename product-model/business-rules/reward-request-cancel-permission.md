---
appliesTo:
- type: entity
  id: reward-request
  effect: removes
permits:
- actors:
  - parent
- related:
  - verb: requests
    entity: family-member
  - verb: is
    entity: kid
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
---

# A waiting request is cancelled only from the asker's own device or a parent's

Wall screens and other people's devices can't cancel someone's request.
