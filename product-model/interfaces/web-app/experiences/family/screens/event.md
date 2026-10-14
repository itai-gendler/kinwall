---
entities:
- entity: event
  shows:
  - Title
  - Starts
  - Ends
  - All day
  - Location
  - Notes
  - Repeat
  - Who
  - Category
  - Reminder
  - Show as
  - Travel time
  collects:
  - Title
  - Starts
  - Ends
  - All day
  - Location
  - Notes
  - Repeat
  - Category
  - Reminder
  - Show as
  - Travel time
- entity: calendar
  shows:
  - Name
  - Writable
  - Members
- entity: family-member
  shows:
  - Name
  - Color
  - Avatar
- entity: list-item
  shows:
  - Title
references:
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#EventDetailSheet
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#EventEditSheet
---

# Event

One event's details: when, where, notes, people, category, reminder, travel time and its tasks, opened from the Board or the calendar.
