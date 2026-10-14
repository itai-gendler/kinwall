---
appliesTo:
- type: entity
  id: bonus-points
  effect: creates
permits:
- actors:
  - parent
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
references:
- kind: code
  role: implementation
  target: server/src/routes/bonus-points.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents give bonus points, while Chores & points is on

Wall screens and kids' devices see bonus points but never give them.
