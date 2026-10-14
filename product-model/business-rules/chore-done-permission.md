---
appliesTo:
- type: entity
  id: chore-completion
  effect: creates
  to: Done
permits:
- actors:
  - parent
- actors:
  - wall-screen
  when:
  - entity: chore
    fact: Needs a parent's OK
    is: 'No'
- actors:
  - wall-screen
  when:
  - entity: chore
    fact: Needs a parent's OK
    is: Default
  - entity: family-member
    fact: Their chores need a parent's OK
    is: 'Off'
- related:
  - verb: earns
    entity: family-member
  - verb: is
    entity: kid
  when:
  - entity: chore
    fact: Needs a parent's OK
    is: 'No'
- related:
  - verb: earns
    entity: family-member
  - verb: is
    entity: kid
  when:
  - entity: chore
    fact: Needs a parent's OK
    is: Default
  - entity: family-member
    fact: Their chores need a parent's OK
    is: 'Off'
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# A tick counts at once from a parent, or elsewhere when no parent's OK is needed

A parent's tick is done straight away. A tick from a wall screen, or from a kid's device for that kid, is done at once only when the chore says No, or follows a person whose chores need no OK.
