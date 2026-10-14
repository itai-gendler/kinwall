---
appliesTo:
- type: entity
  id: recovery-code
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
---

# Only parents retire recovery codes

Generating a new set retires the old codes.
