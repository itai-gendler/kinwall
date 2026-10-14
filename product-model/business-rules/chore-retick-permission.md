---
appliesTo:
- type: entity
  id: chore-completion
  effect: changes
  from: Not yet
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
  target: server/src/routes/chores.ts#completeChore
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# A chore sent back is ticked again by a parent, a wall screen or the kid it credits

After Not yet, a kid's device ticks again only for that kid.
