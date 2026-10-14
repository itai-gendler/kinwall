---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps + on their own device and fills in the event
  kind: actor
  actor: kid
  entities:
  - {entity: calendar, effect: reads, facts: [Name, Members]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The Product adds the Event to the Kid's Calendar
  kind: product
  actor: kid
  entities:
  - {entity: event, effect: creates, to: Shown, facts: [Title, Starts, Ends, All day, Location, Notes, Repeat, Who, Category, Reminder, Show as, Travel
        time]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# A kid adds an event to their own calendar

## Trigger

A kid adds soccer practice.

## Outcome

The event is on the kid's calendar.

## Edge cases

- A kid with no calendar of their own sees "Ask a parent to give you a calendar in Settings → Calendars." in place of +.
