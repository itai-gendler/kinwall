---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens a Family member and changes their name, color, avatar or birthday
  kind: actor
  actor: parent
  entities:
  - {entity: family-member, effect: reads, facts: [Name, Color, Avatar, Birthday]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves the changes everywhere the member shows
  kind: product
  actor: parent
  entities:
  - {entity: family-member, effect: changes, facts: [Name, Color, Avatar, Birthday]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Change a member's details

## Trigger

A kid wants a new color.

## Outcome

Their events, chore column and avatar change on every screen.
