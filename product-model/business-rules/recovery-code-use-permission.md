---
appliesTo:
- type: entity
  id: recovery-code
  effect: changes
  to: Used
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
---

# A recovery code is spent by the parent signing in with it

Using a code is how a parent gets back in when every passkey device is lost.
