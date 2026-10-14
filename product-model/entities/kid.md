---
kind: person
acts: external
relations:
- entity: family-member
  verb: is
  cardinality: one-to-one
references:
- kind: code
  role: implementation
  target: server/src/auth.ts#deviceOwner
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# Kid

A child using their own device: a tablet or phone paired as that kid's. It shows only their own events, chores and lists, ticks their chores, asks for rewards and suggests chores, and never reaches the family's settings.
