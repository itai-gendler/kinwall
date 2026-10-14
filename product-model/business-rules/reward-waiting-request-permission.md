---
appliesTo:
- type: entity
  id: reward-request
  effect: creates
  to: Waiting for OK
permits:
- actors:
  - wall-screen
  when:
  - entity: household
    fact: Chores & points
    is: 'On'
  - entity: household
    fact: Rewards
    is: 'On'
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
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#ownerBlock
---

# Only wall screens and kids' devices make requests that wait for an OK

Redeeming needs Chores & points and Rewards on; a split asked for anywhere but a parent's device always waits.
