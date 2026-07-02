# PII — RETAIL_DWH.PUBLIC.CUSTOMERS

## Detected / declared PII columns

| Column | Type | Notes |
|---|---|---|
| EMAIL | VARCHAR | PII flag present in profiling payload |
| PHONE | VARCHAR | PII flag present in profiling payload |

## Handling guidance
- Treat these fields as **sensitive**: restrict access, apply masking/tokenization where appropriate.
- Validate downstream extracts (e.g., BI exports) to avoid unintended exposure.
