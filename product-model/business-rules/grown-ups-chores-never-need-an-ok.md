---
appliesTo:
- type: capability
  id: edit-family-member
- type: entity
  id: family-member
  facts:
  - Grown-up
  - Their chores need a parent's OK
references:
- kind: code
  role: implementation
  target: server/src/routes/members.ts
---

# A grown-up's chores wait for an OK only when the chore itself says Yes

Marking someone a grown-up turns their own approval default off.
