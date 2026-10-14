---
appliesTo:
- type: capability
  id: tag-event-member
- type: capability
  id: untag-event-member
- type: entity
  id: event
  facts:
  - Who
references:
- kind: code
  role: implementation
  target: server/src/calendar-members.ts
- kind: doc
  role: intent
  target: docs/using/events.md
---

# An event's people are its own tags, else its series', else its calendar's members

Tagging on one event wins over the series, which wins over the calendar.
