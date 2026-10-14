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

# Remove a passkey

Remove a passkey, which also signs out every session it started.
