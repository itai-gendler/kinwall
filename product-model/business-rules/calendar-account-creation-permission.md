---
appliesTo:
- type: entity
  id: calendar-account
  effect: creates
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/oauth.ts
- kind: code
  role: implementation
  target: server/src/routes/accounts.ts
---

# Only parents connect calendar accounts

Connecting Google, Outlook or CalDAV is for a parent, in their own browser.
