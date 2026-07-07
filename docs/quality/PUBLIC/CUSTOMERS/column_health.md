# Column Health — PUBLIC.CUSTOMERS

## Column Health Heatmaps

Legend (deterministic):
- 🟩 Good
- 🟨 Watch
- 🟥 Poor
- ⬜ No data

Heuristic mapping (deterministic and input-bound):
- **Completeness** from `null_rate`: 🟩 (<=1%), 🟨 (>1% and <=5%), 🟥 (>5%)
- **Uniqueness** only evaluated for columns explicitly described as unique identifier in provided descriptions (here: `CUSTOMER_ID`); otherwise ⬜
- **Validity/Consistency** per-column not provided → ⬜
- **PII** from `pii_columns`

| Column | Completeness | Uniqueness | Validity | Consistency | Freshness indicator | PII risk |
|---|---|---|---|---|---|---|
| CUSTOMER_ID | ⬜ | 🟩 | ⬜ | ⬜ | ⬜ | ⬜ |
| EMAIL | 🟨 | ⬜ | ⬜ | ⬜ | ⬜ | 🟥 |
| PHONE | 🟥 | ⬜ | ⬜ | ⬜ | ⬜ | 🟥 |
| COUNTRY | 🟩 | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| LAST_UPDATED | 🟩 | ⬜ | ⬜ | ⬜ | 🟩 | ⬜ |

## PII Risk Indicators

| Column | Classification |
|---|---|
| EMAIL | PII (sensitive) |
| PHONE | PII (sensitive) |

## Duplicate Risk

| Key | Signal |
|---|---|
| CUSTOMER_ID | 12 duplicates detected (see `duplication`) |

## Freshness Indicators

| Column | Signal |
|---|---|
| LAST_UPDATED | Last updated `2026-07-06T17:42:51Z`; max lag 4 hours |
