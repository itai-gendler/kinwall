---
kind: primary
routes:
  web: Web
steps:
- text: The Parent adds each person with a name, Grown-up or Kid, a color and an avatar under Who's in the family?
  kind: actor
  actor: parent
  entities:
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product adds each Family member, the first as a grown-up to start
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: creates, facts: [Name, Color, Avatar, Birthday, Grown-up, Their chores need a parent's OK]}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Add the family in the setup wizard

## Trigger

The wizard asks who is in the family.

## Outcome

Everyone is on the wall; at least one member is needed to go on.
