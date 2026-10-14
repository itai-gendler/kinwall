---
availability:
- place: web-app::administration
- place: web-app::welcome
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#RecoveryCodesSection
---

# Generate recovery codes

Make a set of eight one-time recovery codes, shown once, in Settings → Access or in the setup wizard; any older set stops working.
