# PII — PUBLIC.CUSTOMERS

## PII Assessment

| Finding | Detail |
|---|---|
| PII columns detected | `EMAIL`, `PHONE` |
| Quality flag | high severity: "Sensitive PII columns detected." |

## Sensitive Columns

| Column | Data type | Description | Sample values |
|---|---|---|---|
| EMAIL | VARCHAR | Customer email address | john.smith@email.com, alice@email.com |
| PHONE | VARCHAR | Customer phone number | +33612345678, +33687654321 |

## Risk Classification

No data available (no formal risk tiering beyond PII presence was provided).

## Direct vs Indirect Identifiers

| Column | Classification (based on column meaning only) |
|---|---|
| EMAIL | Direct identifier |
| PHONE | Direct identifier |
