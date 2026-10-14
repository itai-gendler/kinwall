---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns on Show hidden, opens the hidden Event and taps Show again
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product shows it to the family again
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, from: Hidden, to: Shown, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Show an event again from the calendar

## Trigger

A parent hid the wrong event.

## Outcome

The event is back on every screen.
