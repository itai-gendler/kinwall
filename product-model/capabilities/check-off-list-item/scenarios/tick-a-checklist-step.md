---
kind: primary
routes:
  web: Web
steps:
- text: The Kid ticks a List item in Get stuff done
  kind: actor
  actor: kid
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Steps]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
- text: The Product ticks it off for the Kid
  kind: product
  actor: kid
  entities:
  - {entity: list-item, effect: changes, from: Open, to: Checked off, facts: [Checked off by, On sale, Steps]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
---

# Tick an item off in Get stuff done

## Trigger

A kid works through their bedtime routine.

## Outcome

The step is done; when all are, Get stuff done says All done!
