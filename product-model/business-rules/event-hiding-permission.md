---
appliesTo:
- type: entity
  id: event
  effect: changes
  to: Hidden
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts
---

# Only parents hide events

Hiding an event or a series from the whole family is for parents' devices.
