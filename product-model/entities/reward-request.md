---
domain: rewards
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: doc
  role: intent
  target: docs/using/rewards.md
---

# Reward request

Points spent on a reward by one person, or split between several who chip in.

## Information kept

- **Points** — what it cost
- **Shares** — who chips in how many points, for a split
- **Note** — a parent's note when they said not this time
- **Requested** — when it was asked for

## States

### Waiting for OK

The asker's points are set aside until a parent decides.

### Approved

It is on; the points stay spent until it is handed over.

### Given

A parent handed it over.

### Not this time

A parent said no or called it off; the points went back.
