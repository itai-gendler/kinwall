---
availability:
- place: web-app::welcome
references:
- kind: code
  role: implementation
  target: server/src/routes/setup.ts
- kind: code
  role: implementation
  target: web/src/Setup.tsx#WelcomeStep
- kind: doc
  role: intent
  target: docs/getting-started/setup-wizard.md
---

# Set up Kinwall

Claim a new, unclaimed Kinwall for the family with the setup code from the server log, on the phone or computer the parent will manage it from. The setup wizard then goes on to the parent's passkey, recovery codes, household, family members, features, a calendar and starter chores.
