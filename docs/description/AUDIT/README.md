# AUDIT — Business Descriptions

## Data Quality Log (`RETAIL_DWH.AUDIT.DQ_LOG`)

**Description:** Data quality check results and failure tracking

### Columns

| Column | Data Type | Standardized Name | Business Name | Description |
|---|---|---|---|---|
| DQ_LOG_ID | NUMBER(38,0) | dq_log_id | Data Quality Log ID | Surrogate identifier for a data quality log record. |
| BATCH_ID | VARCHAR(50) | batch_id | Batch ID | Identifier for the processing batch associated with the data quality check run. |
| CHECK_NAME | VARCHAR(200) | check_name | Check Name | Name of the data quality check that was executed. |
| TARGET_TABLE | VARCHAR(100) | target_table | Target Table | Name of the target table that the check was executed against. |
| CHECK_TYPE | VARCHAR(50) | check_type | Check Type | Category/type of data quality check performed (e.g., completeness, validity). |
| COLUMN_NAME | VARCHAR(100) | column_name | Column Name | Column evaluated by the data quality check, when applicable. |
| ROWS_CHECKED | NUMBER(38,0) | rows_checked | Rows Checked | Number of rows evaluated by the data quality check. |
| ROWS_FAILED | NUMBER(38,0) | rows_failed | Rows Failed | Number of rows that failed the data quality check. |
| FAILURE_RATE | NUMBER(8,6) | failure_rate | Failure Rate | Proportion of checked rows that failed the check. |
| THRESHOLD_PCT | NUMBER(6,4) | threshold_pct | Threshold Percent | Configured threshold (as a fraction/percent) used to determine pass/fail. |
| STATUS | VARCHAR(20) | status | Status | Outcome status of the data quality check execution. |
| SAMPLE_FAILURES | VARIANT | sample_failures | Sample Failures | Semi-structured sample of failing rows/values captured for investigation. |
| CHECKED_AT | TIMESTAMP_NTZ(9) | checked_at | Checked At | Timestamp when the data quality check was executed/logged. |

---

## Load Log (`RETAIL_DWH.AUDIT.LOAD_LOG`)

**Description:** ETL/ELT pipeline load tracking and lineage log

### Columns

| Column | Data Type | Standardized Name | Business Name | Description |
|---|---|---|---|---|
| LOG_ID | NUMBER(38,0) | log_id | Log ID | Surrogate identifier for a load log record. |
| BATCH_ID | VARCHAR(50) | batch_id | Batch ID | Identifier for the pipeline run or processing batch. |
| PIPELINE_NAME | VARCHAR(100) | pipeline_name | Pipeline Name | Name of the ETL/ELT pipeline that executed. |
| TARGET_SCHEMA | VARCHAR(50) | target_schema | Target Schema | Schema name of the load target. |
| TARGET_TABLE | VARCHAR(100) | target_table | Target Table | Table name of the load target. |
| SOURCE_SYSTEM | VARCHAR(100) | source_system | Source System | Upstream system from which data was extracted. |
| SOURCE_FILE | VARCHAR(500) | source_file | Source File | Source file or object identifier used for ingestion, when applicable. |
| START_TIME | TIMESTAMP_NTZ(9) | start_time | Start Time | Timestamp when the pipeline/load started. |
| END_TIME | TIMESTAMP_NTZ(9) | end_time | End Time | Timestamp when the pipeline/load ended. |
| ROWS_EXTRACTED | NUMBER(38,0) | rows_extracted | Rows Extracted | Number of rows extracted from the source. |
| ROWS_LOADED | NUMBER(38,0) | rows_loaded | Rows Loaded | Number of rows successfully loaded into the target. |
| ROWS_REJECTED | NUMBER(38,0) | rows_rejected | Rows Rejected | Number of rows rejected during load (e.g., validation/parsing failures). |
| ROWS_UPDATED | NUMBER(38,0) | rows_updated | Rows Updated | Number of rows updated in the target (e.g., merge/update operations). |
| STATUS | VARCHAR(20) | status | Status | Outcome status for the pipeline run (e.g., succeeded/failed). |
| ERROR_MESSAGE | VARCHAR(2000) | error_message | Error Message | Error details captured for failed or partially failed runs. |
| TRIGGERED_BY | VARCHAR(100) | triggered_by | Triggered By | Actor or mechanism that initiated the pipeline run (e.g., scheduler/user). |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the log record was created. |
