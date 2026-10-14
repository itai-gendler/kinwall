---
appliesTo:
- type: entity
  id: paired-device
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/keys.ts
---

# Only parents remove paired devices

Removing a device signs it out.
