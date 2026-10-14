---
appliesTo:
- type: entity
  id: list-item
  effect: creates
permits:
- actors:
  - parent
- actors:
  - wall-screen
- related:
  - verb: takes
    entity: family-member
  - verb: is
    entity: kid
- actors:
  - kid
  when:
  - fact: Assign to
    absent: true
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# A kid's device adds items only for itself or nobody

Anyone adds items from any device; a kid's own device assigns them only to that kid or to nobody.
