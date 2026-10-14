---
appliesTo:
- type: entity
  id: event
  effect: removes
permits:
- actors:
  - parent
- actors:
  - wall-screen
  when:
  - entity: calendar
    fact: Wall screens and kids' devices can edit
    is: 'On'
- related:
  - verb: holds
    entity: calendar
  - verb: serves
    entity: family-member
  - verb: is
    entity: kid
  when:
  - entity: calendar
    fact: Wall screens and kids' devices can edit
    is: 'On'
- unattended: true
references:
- kind: code
  role: implementation
  target: server/src/auth.ts#canChangeEvents
- kind: code
  role: implementation
  target: server/src/auth.ts#eventWriteBlock
- kind: doc
  role: intent
  target: docs/using/events.md
---

# Events are deleted by parents, and by wall screens and kids' devices where the calendar allows

Parents' devices change events on every calendar. A wall screen changes events on calendars whose Wall screens and kids' devices can edit is on; a kid's device only on such calendars that are for that kid. Syncing writes the providers' own changes.
