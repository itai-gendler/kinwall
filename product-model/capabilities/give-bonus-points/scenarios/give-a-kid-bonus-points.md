---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Give points, picks a Family member, +10 and "Helped carry groceries"
  kind: actor
  actor: parent
  entities:
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product adds the Bonus points and tells that person's own devices "You got 10 bonus points"
  kind: product
  actor: parent
  entities:
  - {entity: bonus-points, effect: creates, facts: [Points, Note, Day]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Give bonus points

## Trigger

A kid carried in the groceries.

## Outcome

The points count toward today, the week, the leaderboard and the balance.

## Edge cases

- Up to 500 points at a time, for today or an earlier day.
