---
appliesTo:
- type: capability
  id: delete-category
- type: capability
  id: edit-category
- type: entity
  id: event
  facts:
  - Category
references:
- kind: code
  role: implementation
  target: server/src/calendar-categories.ts
- kind: doc
  role: intent
  target: docs/using/categories.md
---

# An event's category is its own, else its series', else a keyword match, else its calendar's default

Keywords match whole words or phrases in the title, ignoring case. Deleting a category sends its events to the next source.
