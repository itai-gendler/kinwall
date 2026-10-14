---
availability:
- place: web-app::administration
domain: calendars
references:
- kind: code
  role: implementation
  target: server/src/routes/oauth.ts
- kind: code
  role: implementation
  target: server/src/routes/accounts.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#CaldavSheet
- kind: doc
  role: intent
  target: docs/calendars/google.md
- kind: doc
  role: intent
  target: docs/calendars/icloud-caldav.md
---

# Connect a calendar account

Connect a Google, Outlook or CalDAV (iCloud, Fastmail, Nextcloud) account so its calendars can be added. Google and Outlook are offered once their sign-in is configured for this Kinwall.
