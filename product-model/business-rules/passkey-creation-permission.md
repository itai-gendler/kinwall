---
appliesTo:
- type: entity
  id: passkey
  effect: creates
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
---

# Only parents add passkeys

A new passkey is registered from a parent device, or with a one-time code a parent made.
