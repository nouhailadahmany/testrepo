# STAGING — Business Descriptions

## Staging Campaign Metrics (Raw) (`RETAIL_DWH.STAGING.STG_CAMPAIGN_METRICS_RAW`)

Raw campaign metrics staging table — multi-platform ingestion

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| RAW_ID | NUMBER(38,0) | Raw ID | Surrogate identifier for the raw staging record. |
| SOURCE_SYSTEM | VARCHAR(50) | Source System | Source system/platform that produced the campaign metrics. |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier for the ingestion batch. |
| REPORT_DATE | VARCHAR(20) | Report Date | Reported date for the metrics record as received from the source. |
| CAMPAIGN_ID | VARCHAR(20) | Campaign ID | Source campaign identifier associated with the metrics record. |
| CHANNEL | VARCHAR(50) | Channel | Channel/platform identifier for the metrics record. |
| IMPRESSIONS | VARCHAR(20) | Impressions (Raw) | Impressions value as received from the source (stored as text in raw staging). |
| CLICKS | VARCHAR(20) | Clicks (Raw) | Clicks value as received from the source (stored as text in raw staging). |
| SPEND | VARCHAR(20) | Spend (Raw) | Spend value as received from the source (stored as text in raw staging). |
| CONVERSIONS | VARCHAR(20) | Conversions (Raw) | Conversions value as received from the source (stored as text in raw staging). |
| RAW_JSON | VARIANT | Raw JSON | Raw semi-structured payload captured from the source record. |
| LOAD_TIMESTAMP | TIMESTAMP_NTZ(9) | Load Timestamp | Timestamp when the record was loaded into the staging table. |
| IS_PROCESSED | BOOLEAN | Is Processed | Indicates whether the raw record has been processed downstream. |
| ERROR_MESSAGE | VARCHAR(500) | Error Message | Error message captured during processing, when applicable. |

## Staging Inventory (Raw) (`RETAIL_DWH.STAGING.STG_INVENTORY_RAW`)

Raw inventory ingestion staging table

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| RAW_ID | NUMBER(38,0) | Raw ID | Surrogate identifier for the raw staging record. |
| SOURCE_SYSTEM | VARCHAR(50) | Source System | Source system that produced the inventory record. |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier for the ingestion batch. |
| SNAPSHOT_DATE | VARCHAR(20) | Snapshot Date | Inventory snapshot date as received from the source (stored as text in raw staging). |
| PRODUCT_ID | VARCHAR(20) | Product ID | Source product identifier for the inventory record. |
| STORE_ID | VARCHAR(20) | Store ID | Source store identifier for the inventory record. |
| CLOSING_STOCK | VARCHAR(10) | Closing Stock (Raw) | Closing stock units as received from the source (stored as text in raw staging). |
| UNITS_RECEIVED | VARCHAR(10) | Units Received (Raw) | Units received as received from the source (stored as text in raw staging). |
| UNITS_DAMAGED | VARCHAR(10) | Units Damaged (Raw) | Units damaged as received from the source (stored as text in raw staging). |
| RAW_JSON | VARIANT | Raw JSON | Raw semi-structured payload captured from the source record. |
| LOAD_TIMESTAMP | TIMESTAMP_NTZ(9) | Load Timestamp | Timestamp when the record was loaded into the staging table. |
| IS_PROCESSED | BOOLEAN | Is Processed | Indicates whether the raw record has been processed downstream. |
| ERROR_MESSAGE | VARCHAR(500) | Error Message | Error message captured during processing, when applicable. |
