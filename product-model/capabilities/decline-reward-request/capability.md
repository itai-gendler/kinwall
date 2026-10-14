---
availability:
- place: web-app::family
domain: rewards
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
---

# Decline a reward request

Say Not this time to a waiting request, or Cancel an approved one that won't happen, with an optional note; every share taken goes back.
