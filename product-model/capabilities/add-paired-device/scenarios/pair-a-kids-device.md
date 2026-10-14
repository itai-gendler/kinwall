---
kind: primary
routes:
  web: Web
steps:
- text: The Kid chooses Set up a wall screen or kid's device
  kind: actor
  actor: kid
  entities:
  - {entity: wall-screen, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
- text: The Product shows a 6-digit code and a QR code for a parent
  kind: product
  actor: kid
  entities:
  - {entity: paired-device, effect: creates, to: Waiting for a parent, facts: [Pairing code]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
- text: The Parent enters the code and a name, picks the kid and taps Add it
  kind: actor
  actor: parent
  entities:
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product pairs the Paired device as that kid's device
  kind: product
  actor: parent
  entities:
  - {entity: paired-device, effect: changes, from: Waiting for a parent, to: Paired, facts: [Name, What it is, Whose device]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The device signs itself in and shows only that kid's things
  kind: condition
  actor: kid
  entities:
  - {entity: paired-device, effect: reads, facts: [What it is, Whose device]}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
---

# Pair a kid's device

## Trigger

A kid gets their own tablet.

## Outcome

The tablet is that kid's device: their events, chores and lists only.

## Edge cases

- Scanning the screen's QR code with a parent's phone opens the same approval.
