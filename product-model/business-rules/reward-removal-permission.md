---
appliesTo:
- type: entity
  id: reward
  effect: removes
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

# Only parents delete rewards

Wall screens and kids' devices can't add, edit or remove rewards.
