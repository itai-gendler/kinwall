---
availability:
- place: web-app::family
domain: calendar
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts#createEvent
- kind: code
  role: implementation
  target: server/src/auth.ts#eventWriteBlock
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#EventEditSheet
- kind: doc
  role: intent
  target: docs/using/events.md
---

# Add an event

Add an event to a calendar this device may change, with its time, place, notes, people, reminder, repeat and category. On a synced calendar it is written to Google, Outlook or CalDAV first.
