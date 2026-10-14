---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen types "milk" in Add item and taps Add
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: [Name, Type]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product adds the List item with the store, aisle and department the family used for milk last time
  kind: product
  actor: wall-screen
  entities:
  - {entity: list-item, effect: creates, to: Open, facts: [Title, Quantity, Store, Aisle, Department, For, Assign to, Added by]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Add groceries

## Trigger

The milk is running out.

## Outcome

Milk is on the list, already in its aisle.

## Edge cases

- A name already open on the list is not added twice by Siri or a barcode scan.
