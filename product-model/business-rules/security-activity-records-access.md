---
appliesTo:
- type: capability
  id: sign-in
- type: capability
  id: sign-out
- type: capability
  id: add-passkey
- type: capability
  id: remove-passkey
- type: capability
  id: generate-recovery-codes
- type: capability
  id: add-paired-device
- type: capability
  id: change-device-owner
- type: capability
  id: remove-paired-device
- type: capability
  id: edit-family-member
- type: entity
  id: security-activity-entry
references:
- kind: code
  role: implementation
  target: server/src/routes/security-events.ts
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# Every change to how the family signs in is recorded in security activity

Sign-ins and sign-outs, passkeys added or removed, recovery codes made or used, devices paired, changed or removed, and who is a grown-up each add an entry saying what happened, who did it and when. The log keeps a year, up to 500 entries, and can't be cleared.
