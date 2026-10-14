---
domain: rewards
relations:
- entity: reward-request
  verb: has
  cardinality: one-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: doc
  role: intent
  target: docs/using/rewards.md
---

# Reward

Something the family decides chore points can buy, such as picking the movie or 15 minutes of screen time.

## Information kept

- **Name** — how it shows up
- **Emoji** — its picture
- **Points** — what it costs
- **For** — everyone, or just the people picked
- **Needs a parent's OK** — whether a request from a wall screen or kid's device waits for a parent (on to start)
- **Limit** — no limit, or up to a number a day or a week for each person

## States

### Active

Offered to the people it is for.

### Archived

Hidden from everyone and kept for history.
