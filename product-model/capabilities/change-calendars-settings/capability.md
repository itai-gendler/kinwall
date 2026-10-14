---
availability:
- place: web-app::administration
domain: calendars
references:
- kind: code
  role: implementation
  target: server/src/default-calendar.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#DefaultCalendarRow
- kind: code
  role: implementation
  target: web/src/Settings.tsx#EventLengthRow
---

# Change calendar settings

Change the settings at the top of Settings → Calendars: the default calendar for new events and how long new events last.
