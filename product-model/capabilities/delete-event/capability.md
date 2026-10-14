---
availability:
- place: web-app::family
domain: calendar
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts#deleteEvent
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#EventDetailSheet
---

# Delete an event

Delete an event; one from Google or Outlook is deleted there too, and a Kinwall repeating event goes as a whole series.
