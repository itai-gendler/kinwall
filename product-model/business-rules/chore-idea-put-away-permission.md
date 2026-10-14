---
appliesTo:
- type: entity
  id: chore-idea
  effect: changes
  to: Put away
permits:
- actors:
  - parent
- actors:
  - wall-screen
- related:
  - verb: suggests
    entity: family-member
  - verb: is
    entity: kid
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# An answer is put away by a parent, a wall screen or the kid's own device

A kid's own device puts away only that kid's answers.
