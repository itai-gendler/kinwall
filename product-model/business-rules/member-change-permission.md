---
appliesTo:
- type: entity
  id: family-member
  effect: changes
  facts:
  - Name
  - Color
  - Avatar
  - Birthday
  - Grown-up
  - Their chores need a parent's OK
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

# Only parents change a family member's details

A member's name, color, avatar, birthday, grown-up switch and approval default are changed from parent devices.
