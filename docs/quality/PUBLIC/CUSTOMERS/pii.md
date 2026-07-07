# PII — RETAIL_DWH.PUBLIC.CUSTOMERS

## Detected PII columns

| Column | Type | Classification |
|---|---|---|
| EMAIL | VARCHAR | PII (contact) |
| PHONE | VARCHAR | PII (contact) |

## Handling guidance
- Restrict access to PII columns and apply masking/tokenization where appropriate.
- Ensure downstream extracts (e.g., BI exports) do not expose raw EMAIL/PHONE.
