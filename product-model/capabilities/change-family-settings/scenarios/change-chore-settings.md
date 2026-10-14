---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks the late completion credit and streak grace and switches the leaderboard, spending points and kids' suggestions on or off
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: [Late completion credit, Streak grace, Leaderboard, Rewards, Kids can suggest chores]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves them for every screen
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Late completion credit, Streak grace, Leaderboard, Rewards, Kids can suggest chores]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Change chore settings

## Trigger

A family prefers no competition and full credit for late chores.

## Outcome

Points, streaks and what kids see follow the new settings.

## Edge cases

- With the leaderboard off, apps hide it and the rank badges; points are still counted.
- With rewards off, Rewards is hidden and requests are refused; rewards and past requests are kept.
