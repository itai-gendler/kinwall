---
kind: edge
routes:
  web: Web
steps:
- text: The Parent taps Connect Google
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: Google turns the sign-in down or the parent cancels it
  kind: condition
  entities:
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product connects nothing and says why
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# The provider turns the sign-in down

## Trigger

A parent cancels at Google's consent page.

## Outcome

No account is added.
