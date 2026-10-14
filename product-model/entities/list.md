---
domain: lists
relations:
- entity: list-item
  verb: holds
  cardinality: one-to-many
- entity: family-member
  verb: serves
  cardinality: many-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: doc
  role: intent
  target: docs/using/lists.md
---

# List

A shared list: Groceries, Shopping, To-do or Reusable, live on every screen.

## Information kept

- **Name** — what it is called
- **Type** — Groceries, Shopping, To-do or Reusable
- **Emoji** — its picture
- **Color** — its color
- **Owners** — whose list it is; nobody means the whole family
- **Keep checked items in place** — whether ticked items stay where they are or move to Done
- **Default** — whether it is the family's default Groceries or Shopping list
- **Open items** — how many items are not ticked off
- **Last done** — for a reusable list, when it was last finished and by whom

## States

### Active

On the Lists tab.

### Archived

Hidden from the Lists tab in the Archived section, ready to restore.
