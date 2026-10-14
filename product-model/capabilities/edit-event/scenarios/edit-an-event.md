---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens an Event, taps Edit and changes its time and notes
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts, Ends, Notes]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product saves only the changed fields, writing them to the provider first on a synced calendar
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, facts: [Starts, Ends, Notes]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Edit an event

## Trigger

Practice moves to 5 PM.

## Outcome

The event shows the new time everywhere, and in Google or Outlook too.

## Edge cases

- A repeating Kinwall event changes as a whole series.
- Notes written back replace the provider's formatting only when the notes changed.
