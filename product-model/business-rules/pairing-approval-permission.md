---
appliesTo:
- type: entity
  id: paired-device
  effect: changes
  to: Paired
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/pair.ts
---

# Only parents approve a pairing code

A screen waiting with a code joins the family only once a parent approves it.
