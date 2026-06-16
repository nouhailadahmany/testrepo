# Schema: STAGING

## Summary
- Tables: 3
- Columns: 46
- Constraints present: true
- Notes: PK constraints present; KEY_COLUMN_USAGE not accessible so PK column mappings not confirmed beyond naming.

## Table classification
| Table | Type | Classification | Confidence | Key candidates | Notes |
|---|---|---|---|---|---|
| STG_CAMPAIGN_METRICS_RAW | BASE TABLE | FACT | low | RAW_ID | Raw landing table; many numeric fields stored as TEXT; includes RAW_JSON and load/process columns. |
| STG_INVENTORY_RAW | BASE TABLE | FACT | low | RAW_ID | Raw landing table; measures stored as TEXT; includes RAW_JSON and load/process columns. |
| STG_SALES_RAW | BASE TABLE | FACT | low | RAW_ID | Raw landing table; measures stored as TEXT; includes RAW_JSON and load/process columns. |

## Relationships
None detected/provided.

## Transformation patterns
### raw_variant
- RAW_JSON

### ingestion_audit
- SOURCE_SYSTEM
- SOURCE_FILE
- BATCH_ID
- LOAD_TIMESTAMP
- ERROR_MESSAGE

### flags
- IS_PROCESSED

### date_as_text
- ORDER_DATE
- SNAPSHOT_DATE
- REPORT_DATE
