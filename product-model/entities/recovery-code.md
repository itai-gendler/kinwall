---
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/recovery.ts
- kind: doc
  role: intent
  target: docs/using/sign-in-and-security.md
---

# Recovery code

One of a set of eight one-time codes that get a parent back in when every passkey device is lost.

## States

### Unused

Still able to sign in once.

### Used

Spent on a sign-in; it never works again.
