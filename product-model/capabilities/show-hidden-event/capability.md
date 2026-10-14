---
availability:
- place: web-app::family
- place: web-app::administration
domain: calendar
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#EditCalendarSheet
- kind: doc
  role: intent
  target: docs/using/calendar.md
---

# Show a hidden event again

Show a hidden event, or its series, again: from the event when a parent shows hidden events, or from the calendar's Hidden events list.
