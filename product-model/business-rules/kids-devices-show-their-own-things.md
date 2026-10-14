---
appliesTo:
- type: capability
  id: view-board
- type: capability
  id: browse-calendar
- type: capability
  id: browse-chores
- type: capability
  id: browse-rewards
references:
- kind: code
  role: implementation
  target: server/src/auth.ts#deviceOwner
- kind: doc
  role: intent
  target: docs/settings/access.md
---

# A kid's device shows only that kid's events, chores and lists

A device that belongs to one kid keeps the Board, calendar, chores and lists to that kid (and Anyone chores); it can't pick its own filter.
