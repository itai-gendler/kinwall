---
domain: calendar
relations:
- entity: family-member
  verb: tags
  cardinality: many-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/events.ts
- kind: doc
  role: intent
  target: docs/using/events.md
---

# Event

Something on the family calendar: a one-off or repeating event, in Kinwall or from a synced calendar.

## Information kept

- **Title** — what it is
- **Starts** — when it starts, or its first day for an all-day event
- **Ends** — when it ends, or its last day
- **All day** — whether it takes whole days
- **Location** — where it is, which opens in maps or a video call
- **Notes** — the event's own description, as plain text
- **Repeat** — how it repeats, if it does
- **Who** — the family members it is for
- **Category** — its category, such as Birthdays or Appointments
- **Reminder** — how long before it a reminder goes out
- **Show as** — busy, or free when it does not take anyone's time
- **Travel time** — how long it takes to get there, which gives a leave-by time

## States

### Shown

The family sees it everywhere events show.

### Hidden

A parent hid it, on its own or with its series; the family no longer sees it.
