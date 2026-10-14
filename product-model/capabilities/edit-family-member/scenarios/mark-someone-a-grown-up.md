---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns on Grown-up for a Family member
  kind: actor
  actor: parent
  entities:
  - {entity: family-member, effect: reads, facts: [Name, Grown-up]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves it and turns off their chores needing a parent's OK, and tells that person's own devices
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: changes, facts: [Grown-up, Their chores need a parent's OK]}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Mark someone a grown-up

## Trigger

An adult was added as a kid.

## Outcome

Their chores never wait for an OK.

## Edge cases

- A grown-up who keeps a private journal or has a full-access device of their own can only stop being a grown-up from their own device.
