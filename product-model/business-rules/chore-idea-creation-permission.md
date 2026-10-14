---
appliesTo:
- type: entity
  id: chore-idea
  effect: creates
permits:
- actors:
  - parent
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Kids can suggest chores
    is: 'On'
- actors:
  - wall-screen
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Kids can suggest chores
    is: 'On'
- related:
  - verb: suggests
    entity: family-member
  - verb: is
    entity: kid
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Kids can suggest chores
    is: 'On'
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# Chore ideas are sent while kids can suggest chores

A kid's own device suggests only for that kid; a wall screen suggests for whoever picks themselves. Both need Chores & points and Kids can suggest chores on.
