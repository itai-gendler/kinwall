---
entities:
- entity: paired-device
  shows:
  - Name
  - What it is
  - Whose device
  - Last used
  collects:
  - Pairing code
  - Name
  - What it is
  - Whose device
- entity: passkey
  shows:
  - Name
  - Added
  - Last used
- recovery-code
- entity: security-activity-entry
  shows:
  - What happened
  - When
entryPoints:
- web-app: /#/settings?tab=access
references:
- kind: code
  role: implementation
  target: web/src/Settings.tsx#DisplaysSection
- kind: code
  role: implementation
  target: web/src/Settings.tsx#PasskeysSection
---

# Access

Settings → Access: paired devices, parent devices and passkeys, recovery codes and the latest security activity.
