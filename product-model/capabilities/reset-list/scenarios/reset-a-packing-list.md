---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps Reset on a reusable List
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product unticks every item and step and notes who finished it last
  kind: product
  actor: wall-screen
  entities:
  - {entity: list-item, effect: changes, from: Checked off, to: Open, facts: [Checked off by, Steps]}
  - {entity: list, effect: changes, facts: [Last done]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Reset a reusable list

## Trigger

The family is home from a trip.

## Outcome

The packing list is ready for next time.

## Edge cases

- Completing a chore resets its reusable checklist for that person and the shared items on its own.
