---
domain: family
relations:
- entity: event
  verb: classifies
  cardinality: one-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/categories.ts
- kind: code
  role: implementation
  target: server/src/calendar-categories.ts
- kind: doc
  role: intent
  target: docs/using/categories.md
---

# Category

An event category, such as 🎂 Birthdays or 🏥 Appointments, that colors and marks events and can find them by keywords in their titles.

## Information kept

- **Name** — what it is called
- **Emoji** — the mark events in it show
- **Color** — overrides the tagged person's color on its events
- **Keywords** — words or phrases that put an event in it when its title has them
