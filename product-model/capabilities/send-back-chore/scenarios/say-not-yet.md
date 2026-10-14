---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Not yet on a Chore completion and writes "Please make the bed properly"
  kind: actor
  actor: parent
  entities:
  - {entity: chore-completion, effect: reads, facts: [Day, Done by]}
  - {entity: chore, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product sends it back unticked with the note and tells the kid's own devices
  kind: product
  actor: parent
  entities:
  - {entity: chore-completion, effect: changes, from: Waiting for OK, to: Not yet, facts: [Not yet note]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Say Not yet

## Trigger

The bed is not made properly.

## Outcome

The kid's card shows "Not yet: Please make the bed properly" until they tick it again.
