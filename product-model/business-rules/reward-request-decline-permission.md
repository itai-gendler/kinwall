---
appliesTo:
- type: entity
  id: reward-request
  effect: changes
  to: Not this time
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

# Only parents decline reward requests

Saying Not this time, or calling off an approved reward, is for parents' devices.
