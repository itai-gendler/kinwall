---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen chooses Set up a wall screen or kid's device
  kind: actor
  actor: wall-screen
  entities:
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
- text: The Product shows a 6-digit code and a QR code for a parent
  kind: product
  actor: wall-screen
  entities:
  - {entity: paired-device, effect: creates, to: Waiting for a parent, facts: [Pairing code]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
- text: The Parent enters the code and a name, picks Wall screen (whole family) and taps Add it
  kind: actor
  actor: parent
  entities:
  - {entity: wall-screen, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product pairs the Paired device as a wall screen for the whole family
  kind: product
  actor: parent
  entities:
  - {entity: paired-device, effect: changes, from: Waiting for a parent, to: Paired, facts: [Name, What it is, Whose device]}
  - {entity: wall-screen, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The screen signs itself in and turns on Use as a wall screen
  kind: condition
  actor: wall-screen
  entities:
  - {entity: paired-device, effect: reads, facts: [What it is, Whose device]}
  contexts:
    web: {place: 'web-app::welcome::pairing'}
---

# Pair a wall screen

## Trigger

A family puts a tablet on the kitchen wall.

## Outcome

The tablet is a wall screen for everyone, without settings.
