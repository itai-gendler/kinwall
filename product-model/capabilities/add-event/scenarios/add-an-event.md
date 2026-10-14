---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps + and fills in the title, time, calendar, location, notes, who, reminder, repeat and category
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Name]}
  - {entity: category, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The Product adds the Event to that Calendar and says "Event added" with View
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: creates, to: Shown, facts: [Title, Starts, Ends, All day, Location, Notes, Repeat, Who, Category, Reminder, Show as, Travel
        time]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# Add an event

## Trigger

A parent books a dentist appointment.

## Outcome

The event shows for everyone tagged.

## Edge cases

- Picking a start fills in the end the family's new event length later.
- With no Kinwall calendar yet, Kinwall only (not synced) creates one called "Kinwall".
