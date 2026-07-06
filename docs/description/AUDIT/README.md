# AUDIT — Business Descriptions

This document provides business-facing descriptions for tables in the `RETAIL_DWH.AUDIT` schema.

## Data Quality Log (`RETAIL_DWH.AUDIT.DQ_LOG`)

Stores data quality check execution results, failures, and related metrics.

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| DQ_LOG_ID | NUMBER(38,0) | Data Quality Log ID | Unique identifier for the data quality log record |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier of the processing batch associated with the check |
| CHECK_NAME | VARCHAR(200) | Check Name | Name of the data quality check executed |
| TARGET_TABLE | VARCHAR(100) | Target Table | Table the data quality check was run against |
| CHECK_TYPE | VARCHAR(50) | Check Type | Category or type of data quality check performed |
| COLUMN_NAME | VARCHAR(100) | Column Name | Column evaluated by the data quality check (if applicable) |
| ROWS_CHECKED | NUMBER(38,0) | Rows Checked | Number of rows evaluated by the data quality check |
| ROWS_FAILED | NUMBER(38,0) | Rows Failed | Number of rows that failed the data quality check |
| FAILURE_RATE | NUMBER(8,6) | Failure Rate | Proportion of checked rows that failed the check |
| THRESHOLD_PCT | NUMBER(6,4) | Threshold Percent | Failure rate threshold used to determine pass/fail |
| STATUS | VARCHAR(20) | Status | Outcome status of the check execution |
| SAMPLE_FAILURES | VARIANT | Sample Failures | Sample of failing records or failure details (semi-structured) |
| CHECKED_AT | TIMESTAMP_NTZ(9) | Checked At | Timestamp when the data quality check was executed |

---

## Load Log (`RETAIL_DWH.AUDIT.LOAD_LOG`)

Tracks ETL/ELT pipeline executions, load counts, status, and errors.

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| LOG_ID | NUMBER(38,0) | Log ID | Unique identifier for the load log record |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier of the processing batch for the pipeline run |
| PIPELINE_NAME | VARCHAR(100) | Pipeline Name | Name of the pipeline or job that performed the load |
| TARGET_SCHEMA | VARCHAR(50) | Target Schema | Schema containing the target table for the load |
| TARGET_TABLE | VARCHAR(100) | Target Table | Target table loaded by the pipeline run |
| SOURCE_SYSTEM | VARCHAR(100) | Source System | Name of the upstream source system for the loaded data |
| SOURCE_FILE | VARCHAR(500) | Source File | Source file or object name used for the load (if applicable) |
| START_TIME | TIMESTAMP_NTZ(9) | Start Time | Timestamp when the pipeline run started |
| END_TIME | TIMESTAMP_NTZ(9) | End Time | Timestamp when the pipeline run ended |
| ROWS_EXTRACTED | NUMBER(38,0) | Rows Extracted | Number of rows extracted from the source |
| ROWS_LOADED | NUMBER(38,0) | Rows Loaded | Number of rows successfully loaded to the target |
| ROWS_REJECTED | NUMBER(38,0) | Rows Rejected | Number of rows rejected during loading |
| ROWS_UPDATED | NUMBER(38,0) | Rows Updated | Number of rows updated in the target during the run |
| STATUS | VARCHAR(20) | Status | Execution status of the pipeline run |
| ERROR_MESSAGE | VARCHAR(2000) | Error Message | Error details captured for failed or problematic runs |
| TRIGGERED_BY | VARCHAR(100) | Triggered By | User, process, or scheduler that initiated the run |
| CREATED_AT | TIMESTAMP_NTZ(9) | Created At | Timestamp when the log record was created |
