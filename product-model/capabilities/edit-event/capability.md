---
availability:
- place: web-app::family
domain: calendar
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts#updateEvent
- kind: code
  role: implementation
  target: server/src/auth.ts#canChangeEvents
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#EventEditSheet
- kind: doc
  role: intent
  target: docs/using/events.md
---

# Edit an event

Change an event's details: title, time, location, notes, reminder, free or busy, repeat, category and travel time. A Kinwall repeating event changes as a whole series; on a synced calendar the change is written back to the provider first.
