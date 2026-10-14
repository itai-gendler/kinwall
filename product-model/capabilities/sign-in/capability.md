---
availability:
- place: web-app::welcome
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
- kind: code
  role: implementation
  target: web/src/App.tsx#RecoveryCodeGate
- kind: doc
  role: intent
  target: docs/using/sign-in-and-security.md
---

# Sign in as a parent

Sign a phone or computer in as a parent device, with a passkey or, when every passkey device is lost, a one-time recovery code. Either gives a 30-day parent session.
