---
appliesTo:
- type: entity
  id: list-item
  effect: changes
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
- related:
  - verb: holds
    entity: list
  - verb: serves
    entity: family-member
  - verb: is
    entity: kid
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
- kind: doc
  role: intent
  target: docs/using/lists.md
---

# A kid's device changes only its own, unassigned or its own list's items

Parents' devices and wall screens work on every item. A kid's own device changes its own items, items assigned to nobody, and anything on a list that belongs to that kid.
