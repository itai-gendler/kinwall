---
appliesTo:
- type: entity
  id: chore-completion
  effect: removes
permits:
- actors:
  - parent
- actors:
  - wall-screen
- related:
  - verb: earns
    entity: family-member
  - verb: is
    entity: kid
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# A tick is taken back by a parent, a wall screen or the kid it credits

A kid's own device unticks only its own chores and the Anyone chores it did.
