---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns on the parent's OK switch for a Family member
  kind: actor
  actor: parent
  entities:
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves it, so that kid's ticks on a wall screen or their own device wait for a parent
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: changes, facts: [Their chores need a parent's OK]}
  - {entity: wall-screen, effect: reads, facts: []}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Make a kid's chores need a parent's OK

## Trigger

A parent wants to check chores before points count.

## Outcome

Chores that follow the person's default now wait for an OK.
