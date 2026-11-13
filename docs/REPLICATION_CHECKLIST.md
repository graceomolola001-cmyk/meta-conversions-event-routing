# Reproducing the Meta conversions workflow

1. Import `workflows/18-meta-conversions.json` into a test n8n workspace.
2. Create a synthetic Google Sheet containing event metadata and **consented**, fictional customer fields.
3. Supply an authorized Meta Dataset/Pixel identifier and a server-side access token privately.
4. Verify event selection, event ID generation, timestamp formatting, identifier normalization and SHA-256 hashing rules.
5. Use Meta's testing mechanism and inspect the HTTP request and response.
6. Verify that browser and server event IDs match when deduplication is intended.
7. Test rejected, malformed or duplicated events, and add reliable error handling before deployment.

**Never place a Meta access token, real phone/email address, Pixel ID or production event payload in a public repository.**
