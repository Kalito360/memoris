# backend

Orchestration layer between AI agents and Shelby.

Handles:
- Memory normalization (structuring raw agent memory into a consistent schema)
- Agent/session tagging
- Calls to Shelby's storage API (S3-compatible writes/reads)
- Composing Memoris receipts (Shelby's native proof + Memoris agent metadata)
- Verification requests (pass-through to Shelby's own proof-checking)

No custom storage, hashing, or blockchain anchoring lives here — that's Shelby's job. This layer is intentionally thin: it structures data before it reaches Shelby, and structures Shelby's response before returning it to the caller.

**Status:** not yet implemented — architecture in progress.
