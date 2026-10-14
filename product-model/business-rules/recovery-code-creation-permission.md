---
appliesTo:
- type: entity
  id: recovery-code
  effect: creates
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
---

# Only parents generate recovery codes

Recovery codes are made from a parent device.
