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
  target: server/src/calendar-members.ts
- kind: doc
  role: intent
  target: docs/using/events.md
---

# Tag someone on an event

Tag a family member on an event, so it shows in their color and on their day. Tags are kept in Kinwall, so they work on read-only events too.
