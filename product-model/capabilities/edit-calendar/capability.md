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
  target: server/src/calendar-filter.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#EditCalendarSheet
- kind: doc
  role: intent
  target: docs/settings/calendars.md
---

# Edit a calendar

Change a calendar's name, color, whose calendar it is, its default category, which of its events the family sees, whether it is on, and whether wall screens and kids' devices can change its events.
