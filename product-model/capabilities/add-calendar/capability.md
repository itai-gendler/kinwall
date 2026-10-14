---
availability:
- place: web-app::administration
domain: calendars
references:
- kind: code
  role: implementation
  target: server/src/routes/calendars.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#RemoteCalendarPicker
- kind: code
  role: implementation
  target: web/src/Settings.tsx#IcsSheet
- kind: code
  role: implementation
  target: web/src/Settings.tsx#LocalCalendarSheet
- kind: doc
  role: intent
  target: docs/settings/calendars.md
- kind: doc
  role: intent
  target: docs/calendars/ics-feeds.md
---

# Add a calendar

Add a calendar to Kinwall: one kept only in Kinwall, an ICS feed by its link, or a calendar from a connected account, with whose calendar it is.
