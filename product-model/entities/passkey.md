---
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/passkeys.ts
- kind: doc
  role: intent
  target: docs/using/sign-in-and-security.md
---

# Passkey

How a parent signs in on a phone or computer, with Face ID, Touch ID, the screen lock or a security key.

## Information kept

- **Name** — the device or security key it lives on
- **Whose device** — the grown-up whose device it is, or no one in particular
- **Added** — when it was registered
- **Last used** — when it last signed someone in
