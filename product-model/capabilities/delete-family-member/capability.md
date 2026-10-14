---
availability:
- place: web-app::family
domain: family
references:
- kind: code
  role: implementation
  target: server/src/routes/members.ts
- kind: doc
  role: intent
  target: docs/settings/family.md
---

# Delete a family member

Remove someone from the family. Their chores, calendars and event tags lose them but stay; a device that was theirs becomes a shared one.
