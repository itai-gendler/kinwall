---
entities:
- entity: calendar
  shows:
  - Name
  - Kind
  - Color
  - Last synced
  - Sync status
  collects:
  - Name
  - Feed link
  - Members
- entity: calendar-account
  shows:
  - Provider
  - Account
  collects:
  - Provider
  - Account
- entity: household
  shows:
  - Default calendar for new events
  - New events last
  collects:
  - Default calendar for new events
  - New events last
entryPoints:
- web-app: /#/settings?tab=calendars
references:
- kind: code
  role: implementation
  target: web/src/Settings.tsx#CalendarsSection
---

# Calendars

Settings → Calendars: the family's calendars and their status, the default calendar and event length, and connecting accounts.
