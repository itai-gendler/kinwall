---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen picks This week on the leaderboard
  kind: actor
  actor: wall-screen
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Wall screen reads each Family member's points, streak and rank
  kind: actor
  actor: wall-screen
  entities:
  - {entity: family-member, effect: reads, facts: [Name, Points earned, Streak, Points to spend]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# See who is ahead this week

## Trigger

The kids want to know who is winning.

## Outcome

Members are ranked by points earned; the leader wears a crown.

## Edge cases

- Someone with no points yet shows no rank, so a fresh day does not put everyone at #1.
