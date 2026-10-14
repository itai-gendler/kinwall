---
appliesTo:
- type: capability
  id: add-paired-device
- type: capability
  id: change-device-owner
- type: entity
  id: paired-device
  facts:
  - Whose device
references:
- kind: code
  role: implementation
  target: server/src/auth.ts#deviceKindOwner
---

# A paired device is a wall screen or a kid's, never a grown-up's

Grown-ups sign in on their own phone or computer with a passkey instead.

## Rationale

A device that belongs to someone opens their private journal, so whoever approves a code must never get a grown-up's.
