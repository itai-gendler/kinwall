---
availability:
- place: web-app::family
- place: web-app::welcome
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

# Add a family member

Add someone who shows up on the wall, with a name, color and avatar, and whether they are a grown-up, in Settings → Family or in the setup wizard.
