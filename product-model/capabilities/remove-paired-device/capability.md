---
availability:
- place: web-app::administration
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/keys.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#DisplaysSection
---

# Remove a paired device

Remove a wall screen or kid's device from the family, which signs it out.
