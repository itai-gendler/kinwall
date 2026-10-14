---
appliesTo:
- type: entity
  id: security-activity-entry
  effect: reads
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/security-events.ts
---

# Only parents read security activity

Wall screens and kids' devices never see the security log.
