---
domain: lists
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: doc
  role: intent
  target: docs/using/lists.md
---

# List item

One thing on a list: a grocery, a to-do or a step of a routine.

## Information kept

- **Title** — what it is
- **Quantity** — how many or how much, such as "2" or "1 lb"
- **Store** — where to buy it
- **Aisle** — where it is in that store
- **Department** — the kind of thing it is, such as Produce
- **On sale** — a sale tag that goes away once it is ticked
- **For** — who a shopping item is for, or everyone
- **Assign to** — who a to-do or routine item belongs to, or nobody
- **Due date** — when a to-do is due
- **Priority** — how important it is
- **Steps** — smaller steps that tick the item when all are done
- **Linked event** — the event it is a task for
- **Notes** — its own description
- **Added by** — who added it and when
- **Checked off by** — who ticked it and when

## States

### Open

Still to do or buy.

### Checked off

Ticked; cleared or reset later.
