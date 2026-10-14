---
kind: primary
routes:
  web: Web
steps:
- text: The Parent enters the family name, timezone and week start under Your household
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product saves them
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Family name, Timezone, Week starts on]}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Parent taps what the family will use Kinwall for under What do you want Kinwall for?
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product turns on the features those cards stand for
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Chores & points, Lists, Features]}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Set up the household in the setup wizard

## Trigger

The wizard asks about the household.

## Outcome

The household is named and only the features the family picked are on.

## Edge cases

- Skip keeps every feature on; with no kids in the family the chores card starts off.
