---
entities:
- entity: household
  collects:
  - Family name
  - Timezone
  - Week starts on
  - Chores & points
  - Lists
  - Features
- entity: passkey
  shows:
  - Name
- recovery-code
- entity: family-member
  shows:
  - Name
  - Color
  - Avatar
  - Grown-up
  collects:
  - Name
  - Color
  - Avatar
  - Grown-up
references:
- kind: code
  role: implementation
  target: web/src/Setup.tsx#WelcomeStep
- kind: code
  role: implementation
  target: web/src/Setup.tsx#PasskeyStep
- kind: code
  role: implementation
  target: web/src/Setup.tsx#RecoveryStep
---

# Setup

The first-run setup wizard: the setup code, a passkey, recovery codes, the household, the family and its features.
