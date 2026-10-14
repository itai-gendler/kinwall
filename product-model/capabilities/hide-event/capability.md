---
availability:
- place: web-app::family
domain: calendar
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#HideSection
- kind: doc
  role: intent
  target: docs/using/calendar.md
---

# Hide an event

Hide an event, or every one in its series, from the whole family, on every screen; it stays hidden across syncs.
