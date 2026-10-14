---
availability:
- place: web-app::administration
- place: web-app::welcome
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#PasskeysSection
- kind: doc
  role: intent
  target: docs/using/sign-in-and-security.md
---

# Add a passkey

Register a passkey: on this phone or computer, or with a security key or a phone nearby, in Settings → Access or as the setup wizard's second step.
