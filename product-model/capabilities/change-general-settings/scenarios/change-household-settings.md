---
kind: primary
routes:
  web: Web
steps:
- text: The Parent changes the family name, timezone, week start or default reminder
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: [Family name, Timezone, Week starts on, Default reminder]}
  contexts:
    web: {place: 'web-app::family::general-settings'}
- text: The Product saves them for every screen and phone
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Family name, Timezone, Week starts on, Default reminder]}
  contexts:
    web: {place: 'web-app::family::general-settings'}
---

# Change household settings

## Trigger

A family moves to another timezone.

## Outcome

Every screen shows the household's new settings.
