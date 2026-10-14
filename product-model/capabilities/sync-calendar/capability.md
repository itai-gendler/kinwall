---
availability:
- place: web-app::administration
domain: calendars
references:
- kind: code
  role: implementation
  target: server/src/sync.ts#syncDue
- kind: code
  role: implementation
  target: server/src/sync.ts#syncCalendar
- kind: code
  role: implementation
  target: server/src/routes/calendars.ts
- kind: doc
  role: intent
  target: docs/calendars/sync.md
---

# Sync a calendar

Bring a synced calendar's events up to date: on its own every few minutes, or now with Sync now. Kinwall keeps events from 30 days back to a year ahead.
