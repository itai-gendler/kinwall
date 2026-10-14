---
domain: family
relations:
- entity: chore
  verb: does
  cardinality: one-to-many
- entity: chore-completion
  verb: earns
  cardinality: one-to-many
- entity: chore-idea
  verb: suggests
  cardinality: one-to-many
- entity: bonus-points
  verb: receives
  cardinality: one-to-many
- entity: reward-request
  verb: requests
  cardinality: one-to-many
- entity: list-item
  verb: takes
  cardinality: one-to-many
- entity: paired-device
  verb: owns
  cardinality: one-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/members.ts
- kind: doc
  role: intent
  target: docs/settings/family.md
---

# Family member

Someone who shows up on the wall: a grown-up or a kid, with the color that marks their events, chores and avatar.

## Information kept

- **Name** — what the family calls them
- **Color** — colors their events, chore column and avatar
- **Avatar** — an emoji, a one or two letter initial, or a picture
- **Birthday** — a date, with or without the year
- **Grown-up** — whether they are one of the adults; a grown-up's chores never wait for a parent's OK
- **Their chores need a parent's OK** — whether their ticks on a wall screen or their own device wait for a parent
- **Points earned** — points earned today, this week and this month, from chores and bonus points
- **Points to spend** — everything they have earned minus what they have spent
- **Streak** — consecutive days on which every chore due for them was done
- **Reward goal** — the reward they are saving for
