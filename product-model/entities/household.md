---
singleton: true
references:
- kind: code
  role: implementation
  target: server/src/routes/settings.ts#readSettings
- kind: code
  role: implementation
  target: server/src/routes/setup.ts
- kind: doc
  role: intent
  target: docs/settings/general.md
---

# Household

The one family a Kinwall serves, with the settings every screen and phone in the house shares.

## Information kept

- **Family name** — shown in the header ("Our Family" to start)
- **Timezone** — the household timezone that "today", chores, reminders and summaries use
- **Week starts on** — Sunday or Monday, for the week and month views and the weekly leaderboard
- **Default reminder** — the reminder an event without its own gets (30 minutes to start)
- **Chores & points** — whether chores, points, rewards and the sticker book are on
- **Lists** — whether lists are on
- **Features** — which other parts of Kinwall are on, such as meals, contacts, notes, photos and check-ins
- **Late completion credit** — the share of its points a chore earns when it is ticked for a past day (50% to start)
- **Streak grace** — how many missed days in any rolling week a streak survives (1 to start)
- **Leaderboard** — whether the chore leaderboard and rank badges show
- **Rewards** — whether kids can spend points on rewards
- **Kids can suggest chores** — whether kids can send chore ideas
- **Default stores** — the store a shopping trip starts at for Groceries lists and for other shopping lists
- **Default calendar for new events** — where new events go unless someone picks another calendar, or Automatic
- **New events last** — how long a new event lasts when only its start is picked (1 hour to start)

## States

### Unclaimed

A new Kinwall nobody has set up yet; the first browser to open it gets the setup wizard.

### Set up

Claimed by the family; screens and phones sign in or pair to use it.
