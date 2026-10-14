---
appliesTo:
- type: entity
  id: paired-device
  effect: changes
  facts:
  - What it is
  - Whose device
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/keys.ts
---

# Only parents change what a paired device is

The device itself can never change whose it is.
