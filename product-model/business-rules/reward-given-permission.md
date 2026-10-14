---
appliesTo:
- type: entity
  id: reward-request
  effect: changes
  to: Given
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

# Only parents mark rewards given

Handing over is marked from parents' devices.
