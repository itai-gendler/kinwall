---
appliesTo:
- type: entity
  id: event
  effect: changes
  from: Hidden
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts
---

# Only parents show hidden events again

Only parents' devices see hidden events and show them again.
