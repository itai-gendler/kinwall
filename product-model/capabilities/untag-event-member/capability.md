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
  target: web/src/Calendar.tsx#EventDetailSheet
---

# Untag someone from an event

Take a family member's tag off an event.
