---
appliesTo:
- type: entity
  id: passkey
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
---

# Only parents remove passkeys

Removing a passkey is for parent devices.
