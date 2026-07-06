# STAGING — Business Descriptions

This document contains business descriptions for tables in the `RETAIL_DWH.STAGING` schema.

## Staging Campaign Metrics (Raw) (`STG_CAMPAIGN_METRICS_RAW`)

**Fully qualified name:** `RETAIL_DWH.STAGING.STG_CAMPAIGN_METRICS_RAW`

**Description:** Raw, multi-platform campaign metrics landing table prior to transformation.

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| RAW_ID | NUMBER(38,0) | Raw ID | Unique identifier for the raw ingestion record |
| SOURCE_SYSTEM | VARCHAR(50) | Source System | Originating platform or system for the ingested metrics |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier for the ingestion/load batch |
| REPORT_DATE | VARCHAR(20) | Report Date | Reported date for the metric snapshot (raw format) |
| CAMPAIGN_ID | VARCHAR(20) | Campaign ID | Identifier of the marketing campaign (raw) |
| CHANNEL | VARCHAR(50) | Channel | Marketing channel or platform (raw) |
| IMPRESSIONS | VARCHAR(20) | Impressions | Number of impressions recorded (raw text) |
| CLICKS | VARCHAR(20) | Clicks | Number of clicks recorded (raw text) |
| SPEND | VARCHAR(20) | Spend | Advertising spend amount (raw text) |
| CONVERSIONS | VARCHAR(20) | Conversions | Number of conversions recorded (raw text) |
| RAW_JSON | VARIANT | Raw JSON | Original payload captured for the record (semi-structured) |
| LOAD_TIMESTAMP | TIMESTAMP_NTZ(9) | Load Timestamp | Timestamp when the record was loaded into staging |
| IS_PROCESSED | BOOLEAN | Is Processed | Indicates whether the record has been processed downstream |
| ERROR_MESSAGE | VARCHAR(500) | Error Message | Processing/validation error captured for the record |

## Staging Inventory (Raw) (`STG_INVENTORY_RAW`)

**Fully qualified name:** `RETAIL_DWH.STAGING.STG_INVENTORY_RAW`

**Description:** Raw inventory landing table prior to transformation and standardization.

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| RAW_ID | NUMBER(38,0) | Raw ID | Unique identifier for the raw ingestion record |
| SOURCE_SYSTEM | VARCHAR(50) | Source System | Originating system for the inventory snapshot |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier for the ingestion/load batch |
| SNAPSHOT_DATE | VARCHAR(20) | Snapshot Date | Date the inventory snapshot represents (raw format) |
| PRODUCT_ID | VARCHAR(20) | Product ID | Identifier of the product (raw) |
| STORE_ID | VARCHAR(20) | Store ID | Identifier of the store/location (raw) |
| CLOSING_STOCK | VARCHAR(10) | Closing Stock | Closing stock quantity (raw text) |
| UNITS_RECEIVED | VARCHAR(10) | Units Received | Units received quantity (raw text) |
| UNITS_DAMAGED | VARCHAR(10) | Units Damaged | Units damaged quantity (raw text) |
| RAW_JSON | VARIANT | Raw JSON | Original payload captured for the record (semi-structured) |
| LOAD_TIMESTAMP | TIMESTAMP_NTZ(9) | Load Timestamp | Timestamp when the record was loaded into staging |
| IS_PROCESSED | BOOLEAN | Is Processed | Indicates whether the record has been processed downstream |
| ERROR_MESSAGE | VARCHAR(500) | Error Message | Processing/validation error captured for the record |

## Staging Sales (Raw) (`STG_SALES_RAW`)

**Fully qualified name:** `RETAIL_DWH.STAGING.STG_SALES_RAW`

**Description:** Raw sales landing table used to store ingested transactions before transformation.

### Columns

| Column | Data type | Business name | Description |
|---|---|---|---|
| RAW_ID | NUMBER(38,0) | Raw ID | Unique identifier for the raw ingestion record |
| SOURCE_SYSTEM | VARCHAR(50) | Source System | Originating system for the sales data |
| SOURCE_FILE | VARCHAR(200) | Source File | Source file/object name from which the record was ingested |
| BATCH_ID | VARCHAR(50) | Batch ID | Identifier for the ingestion/load batch |
| ORDER_ID | VARCHAR(30) | Order ID | Order identifier from the source (raw) |
| ORDER_LINE_ID | VARCHAR(30) | Order Line ID | Order line identifier from the source (raw) |
| ORDER_DATE | VARCHAR(30) | Order Date | Order date/time value as received from the source (raw) |
| CUSTOMER_ID | VARCHAR(20) | Customer ID | Identifier of the customer (raw) |
| PRODUCT_ID | VARCHAR(20) | Product ID | Identifier of the product sold (raw) |
| STORE_ID | VARCHAR(20) | Store ID | Identifier of the store/location (raw) |
| QUANTITY | VARCHAR(10) | Quantity | Quantity sold (raw text) |
| UNIT_PRICE | VARCHAR(20) | Unit Price | Price per unit (raw text) |
| DISCOUNT_CODE | VARCHAR(30) | Discount Code | Discount or promotion code applied (raw) |
| PAYMENT_METHOD | VARCHAR(50) | Payment Method | Payment method used for the order (raw) |
| SHIPPING_COUNTRY | VARCHAR(5) | Shipping Country | Destination country code for shipping (raw) |
| RAW_JSON | VARIANT | Raw JSON | Original payload captured for the record (semi-structured) |
| LOAD_TIMESTAMP | TIMESTAMP_NTZ(9) | Load Timestamp | Timestamp when the record was loaded into staging |
| IS_PROCESSED | BOOLEAN | Is Processed | Indicates whether the record has been processed downstream |
| ERROR_MESSAGE | VARCHAR(500) | Error Message | Processing/validation error captured for the record |
