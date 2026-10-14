---
appliesTo:
- type: entity
  id: family-member
  effect: removes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/members.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents delete family members

Deleting someone from the family is for parent devices.
