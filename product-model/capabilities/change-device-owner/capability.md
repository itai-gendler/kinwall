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
  target: server/src/auth.ts#deviceKindOwner
- kind: code
  role: implementation
  target: web/src/Settings.tsx#DeviceKindSelect
---

# Change what a paired device is

Change a paired device between a wall screen for the whole family and one kid's device, from the parent's list of paired devices. The device itself can't change it.
