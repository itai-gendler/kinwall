---
availability:
- place: web-app::family
domain: calendar
references:
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#CalendarView
- kind: code
  role: implementation
  target: server/src/routes/events.ts#eventInstances
- kind: doc
  role: intent
  target: docs/using/calendar.md
---

# Browse the calendar

See every calendar's events merged and colored by person, in Day, Week, Month and Schedule views (3 Day on phones), filtered by person or category.
