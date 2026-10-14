---
availability:
- place: web-app::administration
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#PasskeysSection
---

# Sign out

End this phone or computer's passkey session.
