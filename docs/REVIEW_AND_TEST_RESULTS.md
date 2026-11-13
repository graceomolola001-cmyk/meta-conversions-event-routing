# Review findings and test evidence

Reviewed November 13, 2026. Offline JavaScript checks exposed that the original event builder could emit missing hashed identifiers and treat a raw click ID as a formatted Meta `fbc`. The public builder has now been hardened to reject absent/invalid hashed identifiers, require a stable lead ID and timestamp, and omit an unformatted click ID.

## Preconditions for execution

- Reconnect a **test** Google Sheet and Meta server-side credential.
- Validate Meta's currently supported endpoint version and event schema in its official documentation.
- Confirm that the Crypto nodes produce SHA-256 hexadecimal hashes with correct normalization.
- Send consented synthetic/test events only.
- Ensure browser and server conversion event IDs align if deduplication is intended.
- Implement exception reporting, retry behavior and idempotency before production.
- Verify that payment status is **independently verified**, not merely claimed.

## What remains unverified

No Meta Graph API request was sent during this review. The event payload, data-use permissions, current API schema and server response must be checked in Meta Test Events before deployment. Static syntax does not prove attribution accuracy or accepted CAPI events.
