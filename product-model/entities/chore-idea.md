---
domain: chores
relations:
- entity: chore
  verb: becomes
  cardinality: one-to-one
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Chore idea

A chore a kid suggests, with the points they think it is worth, for a grown-up to say yes to or not.

## Information kept

- **Title** — what they want to do
- **Emoji** — its picture
- **Points asked** — what they think it is worth (0 to 100)
- **Repeat** — the days it would repeat, if it should
- **Day** — the day it is for, or the day a repeat starts
- **Start time** — when it would start
- **Timer** — how long it takes
- **Already did it** — whether they did it already today
- **Note** — the grown-up's note back
- **Answered by** — the grown-up who answered, when their device is theirs

## States

### Waiting for a grown-up

Sent and not answered; it is not a chore yet.

### Approved

A grown-up said yes and made it a chore.

### Not this time

A grown-up said no, with an optional note.

### Put away

The kid read the answer and put it away.
