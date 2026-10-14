---
entities:
- entity: passkey
  shows:
  - Name
- recovery-code
references:
- kind: code
  role: implementation
  target: web/src/App.tsx#PairingGate
- kind: code
  role: implementation
  target: web/src/App.tsx#RecoveryCodeGate
---

# Sign-in

Welcome home: sign in as a parent with a passkey or a recovery code, or set this device up as a wall screen or kid's device.
