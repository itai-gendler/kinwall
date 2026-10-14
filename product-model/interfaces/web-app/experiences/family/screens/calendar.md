---
entities:
- entity: event
  shows:
  - Title
  - Starts
  - Ends
  - All day
  - Who
  - Category
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
  - Who
  - Category
  - Reminder
  - Show as
  - Travel time
- entity: calendar
  shows:
  - Name
  - Kind
  - Members
  - Wall screens and kids' devices can edit
- entity: family-member
  shows:
  - Name
  - Color
  - Avatar
- entity: category
  shows:
  - Name
  - Emoji
  - Color
entryPoints:
- web-app: /#/calendar
references:
- kind: code
  role: implementation
  target: web/src/Calendar.tsx#CalendarView
---

# Calendar

Every calendar's events merged by person in Day, Week, Month and Schedule views, where new events are added.
