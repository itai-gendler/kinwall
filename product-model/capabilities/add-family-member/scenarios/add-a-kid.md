---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Add member and enters a name, color, avatar and birthday
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product adds the Family member as a kid whose chores count without a parent's OK
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: creates, facts: [Name, Color, Avatar, Birthday, Grown-up, Their chores need a parent's OK]}
  - {entity: chore, effect: reads, facts: []}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Add a kid

## Trigger

A family sets up who is in it.

## Outcome

The new member has a column on Chores and a color on the calendar.

## Edge cases

- When two people's colors would look alike to someone with color blindness, a note under the list says so and suggests another color.
