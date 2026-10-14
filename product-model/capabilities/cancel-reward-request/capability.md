---
availability:
- place: web-app::family
domain: rewards
references:
- kind: code
  role: implementation
  target: server/src/routes/rewards.ts
---

# Cancel a reward request

Take back a request still waiting for a parent's OK, from the asker's own device or a parent's. The points come back and the request is gone.
