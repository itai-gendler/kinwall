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
  target: web/src/Settings.tsx#CalendarsSection
---

# Remove a calendar

Remove a calendar and its events from Kinwall; nothing is deleted from the original calendar.
