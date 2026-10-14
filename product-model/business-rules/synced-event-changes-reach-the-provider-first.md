---
appliesTo:
- type: capability
  id: add-event
- type: capability
  id: edit-event
- type: capability
  id: delete-event
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts#updateEvent
- kind: doc
  role: intent
  target: docs/calendars/writable-vs-read-only.md
---

# A change to a synced event is saved in Google, Outlook or CalDAV first

When the provider refuses or can't be reached, nothing is stored in Kinwall. People, category and travel time are Kinwall's own and never go to the provider.
