---
id: kinwall
summary: 'A self-hosted family life organizer for a wall tablet and every phone: shared calendars, chores with points and rewards, and shared lists.'
category: family-organizer
tags:
- family
- calendar
- chores
- lists
- self-hosted
- wall-display
authors:
- name: John Duprey
  url: https://github.com/JohnDuprey
license: AGPL-3.0-or-later
limitations:
- 'Each Kinwall serves one family: parents sign in with a passkey, and wall screens and kids'' devices pair with a code a parent approves; there are no
  usernames or passwords.'
- Wall screens and kids' devices never change the family's settings, calendar setup or who can reach Kinwall; those are for parents' devices.
- Events from ICS feeds are read-only; Google, Outlook and CalDAV calendars sync both ways, and an event is never moved to another calendar from Kinwall.
- 'Bonus points only add: points come off only by spending them, taking a bonus back or unticking a chore.'
- A feature the family turns off is hidden on every screen, never deleted.
languages:
- en
references:
- kind: doc
  role: context
  target: README.md
- kind: doc
  role: context
  target: SPEC.md
- kind: doc
  role: intent
  target: docs/getting-started/what-is-kinwall.md
---

# Kinwall

Kinwall keeps a household's moving parts in one calm place. A tablet on the wall shows the family's day from across the room, and every phone carries
the same thing: calendars from Google, Outlook, iCloud and ICS feeds merged and colored by person, one-off and repeating chores that earn points kids
spend on rewards, and shared grocery, shopping, to-do and reusable lists. Parents manage it from their own phones; wall screens and kids' devices tick
chores off, work on lists and ask for rewards, and a kid's own device shows only that kid's things.

## Intent

"It's not one more app for one busy grown-up; it's where the whole family keeps its plans, so nobody has to carry it all in their head." Kinwall is
built to be used by kids, not just about them, with neurodivergent family members in mind: chores that forgive (late still earns partial credit and a
streak survives an off day), no ads, no tracking and no dark patterns, and the family's data on its own server.
