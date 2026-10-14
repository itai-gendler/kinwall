---
kind: edge
routes:
  web: Web
steps:
- text: The Kid taps a Chore whose checklist still has open items
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Title, Checklist]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: Items on the checklist for the Kid are still open
  kind: condition
  actor: kid
  entities:
  - {entity: list-item, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product opens the checklist in Get stuff done instead of completing the chore
  kind: product
  actor: kid
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
---

# A chore with open checklist items opens its checklist

## Trigger

A kid taps Bedtime before brushing their teeth.

## Outcome

The chore stays open; the checklist is on screen to tick off.
