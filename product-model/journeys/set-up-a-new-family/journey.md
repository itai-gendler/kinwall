---
actors:
- parent
references:
- kind: code
  role: implementation
  target: web/src/Setup.tsx
- kind: code
  role: implementation
  target: server/src/routes/setup.ts
- kind: doc
  role: intent
  target: docs/getting-started/setup-wizard.md
---

# Set up a new family

## Goal

A parent claims a new Kinwall and sets the family up in it: a way back in, the household and who is in the family.

## Success criterion

Kinwall is claimed, the parent has a passkey and recovery codes, and the household and its members are saved.
