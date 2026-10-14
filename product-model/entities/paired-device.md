---
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/pair.ts
- kind: code
  role: implementation
  target: server/src/routes/keys.ts
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# Paired device

A wall screen, or a kid's tablet or phone, joined to the family with a code a parent approves.

## Information kept

- **Pairing code** — the 6-digit code the screen shows while it waits, good for 10 minutes
- **Name** — what the parent called it, such as "Kitchen wall"
- **What it is** — a wall screen for the whole family, or a kid's device
- **Whose device** — the kid it belongs to, or shared
- **Last used** — when it last reached Kinwall

## States

### Waiting for a parent

The screen shows its code and waits for a parent to approve it.

### Paired

Approved: the screen is signed in as a wall screen or as that kid's device.
