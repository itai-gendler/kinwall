---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Manage rewards, then Add reward, and fills in "📺 15 min screen time", 20 points, up to 3 a day
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product adds the Reward for the people it is for
  kind: product
  actor: parent
  entities:
  - {entity: reward, effect: creates, to: Active, facts: [Name, Emoji, Points, For, Needs a parent's OK, Limit]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Add a reward

## Trigger

A family decides what points can buy.

## Outcome

The kids see the new reward and how many points it needs.

## Edge cases

- With no rewards yet, a parent sees four one-tap suggestions.
