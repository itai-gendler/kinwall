---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps Suggest a chore, types it, picks an emoji and points, checks I already did it today and taps Send to a grown-up
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product saves the Chore idea as Waiting for a grown-up and tells parents' devices
  kind: product
  actor: kid
  entities:
  - {entity: chore-idea, effect: creates, to: Waiting for a grown-up, facts: [Title, Emoji, Points asked, Repeat, Day, Start time, Timer, Already did it]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Suggest a chore

## Trigger

A kid wants piano practice on the chart.

## Outcome

The idea shows under Chore ideas; it is not a chore yet.
