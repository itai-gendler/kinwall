---
availability:
- place: web-app::administration
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/security-events.ts
- kind: code
  role: implementation
  target: web/src/SecurityActivitySheet.tsx
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# View security activity

Read the family's security log: sign-ins and sign-outs, passkeys, recovery codes, paired devices, whose device something is and who is a grown-up.
