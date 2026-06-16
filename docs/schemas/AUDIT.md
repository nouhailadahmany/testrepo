# Schema: AUDIT

## Summary
- Tables: 2
- Columns: 30
- Constraints present: true
- Notes: TABLE_CONSTRAINTS returned PKs; KEY_COLUMN_USAGE not accessible, so PK/FK column mappings unavailable.

## Table classification
| Table | Type | Classification | Confidence | Key candidates | Notes |
|---|---|---|---|---|---|
| DQ_LOG | BASE TABLE | FACT | medium | DQ_LOG_ID | Log/metrics table with counts/rates/timestamps. |
| LOAD_LOG | BASE TABLE | FACT | medium | LOG_ID | Pipeline load metrics (rows_, timestamps, status). |

## Relationships
None detected/provided.

## Transformation patterns
### metrics
- ROWS_EXTRACTED
- ROWS_LOADED
- ROWS_REJECTED
- ROWS_UPDATED
- ROWS_CHECKED
- ROWS_FAILED
- FAILURE_RATE

### timestamps
- START_TIME
- END_TIME
- CREATED_AT
- CHECKED_AT

### keys
- DQ_LOG_ID
- LOG_ID
- BATCH_ID
