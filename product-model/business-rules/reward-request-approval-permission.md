---
appliesTo:
- type: entity
  id: reward-request
  effect: changes
  to: Approved
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents approve reward requests

Approving is for parents' devices.
