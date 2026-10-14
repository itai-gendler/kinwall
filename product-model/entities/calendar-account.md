---
domain: calendars
relations:
- entity: calendar
  verb: provides
  cardinality: one-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/accounts.ts
- kind: code
  role: implementation
  target: server/src/routes/oauth.ts
- kind: doc
  role: intent
  target: docs/settings/calendars.md
---

# Calendar account

A Google, Outlook or CalDAV (iCloud, Fastmail, Nextcloud) account a parent connected, whose calendars Kinwall can add.

## Information kept

- **Provider** — Google, Outlook or CalDAV
- **Account** — the account's name or address
