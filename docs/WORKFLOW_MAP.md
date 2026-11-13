# Node-by-node Meta event map

The seven-node `META CONVERSIONS` workflow includes:

| Node | Role |
| --- | --- |
| Google Sheets Trigger | Ingests a potential conversion event |
| If payment occured | Filters for payment-related events |
| prepare capi data | Formats data for Meta CAPI |
| Crypto and Crypto1 | Hashes designated identifiers |
| send CAPI event | Prepares the request |
| HTTP Request | Sends the configured request to the Graph API |

**Important:** Review exactly which customer fields are normalized and hashed in the Code and Crypto nodes before running a real event. The Pixel ID and API token are placeholders. Verify legal basis, consent, event IDs, response handling and deduplication.
