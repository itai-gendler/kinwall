---
appliesTo:
- type: entity
  id: reward-request
  effect: creates
  to: Approved
permits:
- actors:
  - parent
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Rewards
    is: 'On'
- actors:
  - wall-screen
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Rewards
    is: 'On'
  - entity: reward
    fact: Needs a parent's OK
    is: 'Off'
  - fact: Shares
    absent: true
- related:
  - verb: requests
    entity: family-member
  - verb: is
    entity: kid
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Rewards
    is: 'On'
  - entity: reward
    fact: Needs a parent's OK
    is: 'Off'
  - fact: Shares
    absent: true
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# A reward is approved at once from a parent, or elsewhere when it needs no OK and isn't split

Redeeming needs Chores & points and Rewards on. A kid's own device redeems only for that kid.
