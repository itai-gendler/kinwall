---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps Split it, picks who is chipping in and how much, and taps Ask a grown-up
  kind: actor
  actor: wall-screen
  entities:
  - {entity: reward, effect: reads, facts: [Name, Points]}
  - {entity: family-member, effect: reads, facts: [Name, Points to spend]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product takes the asker's share now and saves the Reward request waiting for a parent
  kind: product
  actor: wall-screen
  entities:
  - {entity: reward-request, effect: creates, to: Waiting for OK, facts: [Points, Shares, Requested]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Split a reward

## Trigger

Two kids pool points for a family movie night.

## Outcome

The request waits for a parent even if the reward needs no OK; the others pay when it is approved.
