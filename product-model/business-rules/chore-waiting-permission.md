---
appliesTo:
- type: entity
  id: chore-completion
  effect: creates
  to: Waiting for OK
permits:
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

# Only wall screens and kids' devices make ticks that wait for an OK

A tick from a wall screen, or from a kid's device for that kid, waits for a parent's OK when the chore or the person needs one; a parent's tick never waits.
