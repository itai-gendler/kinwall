---
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/security-events.ts
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# Security activity entry

One line of the family's security log: a sign-in, a passkey, recovery codes, a paired device, whose device something is, or who is a grown-up.

## Information kept

- **What happened** — in plain words, such as "Passkey "iPhone" added"
- **Who did it** — the person or device that did it, when known
- **Device** — the passkey, key or device it is about
- **When** — when it happened
