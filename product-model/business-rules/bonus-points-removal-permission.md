---
appliesTo:
- type: entity
  id: bonus-points
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/bonus-points.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents take back bonus points

Taking back a bonus is for parents' devices.
