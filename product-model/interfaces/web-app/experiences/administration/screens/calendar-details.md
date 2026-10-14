---
entities:
- entity: calendar
  shows:
  - Name
  - Kind
  - Color
  - Members
  - Default category
  - Filter
  - Enabled
  - Wall screens and kids' devices can edit
  - Writable
  collects:
  - Name
  - Color
  - Members
  - Default category
  - Filter
  - Enabled
  - Wall screens and kids' devices can edit
- entity: event
  shows:
  - Title
  - Starts
- entity: category
  shows:
  - Name
references:
- kind: code
  role: implementation
  target: web/src/Settings.tsx#EditCalendarSheet
---

# Calendar details

Edit calendar: one calendar's name, color, members, default category, filter, switches and hidden events.
