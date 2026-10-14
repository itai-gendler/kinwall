---
domain: chores
relations:
- entity: chore-completion
  verb: has
  cardinality: one-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Chore

A one-off or repeating job for one family member or for anyone, worth points when it is done.

## Information kept

- **Title** — what to do
- **Emoji** — its picture
- **Points** — what it is worth
- **Assigned to** — one family member, or Anyone
- **Repeat** — once, daily, weekly on chosen days or another rule, with an optional last day
- **Due date** — the day a one-off chore is due, or the day a repeat starts
- **Start time** — when it should start on each day it is due
- **Timer** — how long it takes
- **Checklist** — a list that has to be ticked off before the chore can be done
- **Needs a parent's OK** — Default (follow the person), Yes or No

## States

### Active

On the chart on the days it is due.

### Archived

Deleted after it was done: off every list, while its history and points stay.
