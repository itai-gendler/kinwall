---
appliesTo:
- type: entity
  id: family-member
  effect: creates
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

# Only parents add family members

Adding someone to the family is for parent devices; wall screens and kids' devices only read the family.
