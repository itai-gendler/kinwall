---
availability:
- place: web-app::family
domain: family
references:
- kind: code
  role: implementation
  target: server/src/routes/members.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#MemberEditSheet
- kind: doc
  role: intent
  target: docs/settings/family.md
---

# Edit a family member

Change a family member's name, color, avatar or birthday, whether they are a grown-up, and whether their chores need a parent's OK.
