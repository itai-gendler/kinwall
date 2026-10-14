---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Not this time on a Reward request and writes "Let's do it on Friday"
  kind: actor
  actor: parent
  entities:
  - {entity: reward-request, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product gives the points back and tells the person's own devices with the note
  kind: product
  actor: parent
  entities:
  - {entity: reward-request, effect: changes, from: Waiting for OK, to: Not this time, facts: [Note]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Say Not this time to a request

## Trigger

Not today.

## Outcome

The kid has their points back and sees the note on their own device.
