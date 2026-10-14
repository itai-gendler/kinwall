---
kind: primary
result: achieved
routes:
  web: Web
steps:
- text: The Parent enters the setup code and continues
  kind: actor
  actor: parent
  capability: set-up-kinwall
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product claims Kinwall and moves on to the passkey step
  kind: product
  actor: parent
  capability: set-up-kinwall
  entities:
  - {entity: household, effect: changes, from: Unclaimed, to: Set up, facts: []}
  - {entity: passkey, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Parent creates a passkey for this device
  kind: actor
  actor: parent
  capability: add-passkey
  entities:
  - {entity: passkey, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product saves the Passkey and moves on to the recovery codes
  kind: product
  actor: parent
  capability: add-passkey
  entities:
  - {entity: passkey, effect: creates, facts: [Name, Whose device, Added]}
  - {entity: recovery-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product makes eight recovery codes and shows them
  kind: product
  actor: parent
  capability: generate-recovery-codes
  entities:
  - {entity: recovery-code, effect: creates, to: Unused, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Parent saves them and enters the family name, timezone and week start
  kind: actor
  actor: parent
  capability: change-general-settings
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product saves the Household
  kind: product
  actor: parent
  capability: change-general-settings
  entities:
  - {entity: household, effect: changes, facts: [Family name, Timezone, Week starts on]}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Parent adds each person in the family
  kind: actor
  actor: parent
  capability: add-family-member
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product adds each Family member
  kind: product
  actor: parent
  capability: add-family-member
  entities:
  - {entity: family-member, effect: creates, facts: [Name, Color, Avatar, Birthday, Grown-up, Their chores need a parent's OK]}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Go through the setup wizard

## Trigger

A parent opens a Kinwall nobody has set up yet.

## Outcome

The family is set up; the wizard goes on to features, a calendar and starter chores, each of which can be skipped.
