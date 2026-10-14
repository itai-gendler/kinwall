---
kind: primary
routes:
  web: Web
steps:
- text: The Parent deletes a Family member and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product removes the member, takes them off calendars and their chores, and makes their own devices shared
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: removes}
  - {entity: calendar, effect: changes, facts: [Members]}
  - {entity: chore, effect: changes, facts: [Assigned to]}
  - {entity: paired-device, effect: changes, facts: [Whose device]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Delete a family member

## Trigger

Someone no longer lives with the family.

## Outcome

Their chores and events stay, without them.
