---
actors:
- parent
references:
- kind: code
  role: implementation
  target: server/src/routes/oauth.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#RemoteCalendarPicker
- kind: doc
  role: intent
  target: docs/calendars/google.md
---

# Connect a calendar

## Goal

A parent gets a calendar from their Google, Outlook or iCloud account onto the family's screens.

## Success criterion

The account's calendar is added, tagged with its people, and syncs on the next sync.
