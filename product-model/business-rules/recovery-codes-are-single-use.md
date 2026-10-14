---
appliesTo:
- type: capability
  id: sign-in
- type: capability
  id: generate-recovery-codes
- type: entity
  id: recovery-code
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
---

# A recovery code signs in once

A used code never works again, and generating a new set retires the old one at once.
