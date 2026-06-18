# CORE — Business Descriptions

## Campaign Dimension (`RETAIL_DWH.CORE.DIM_CAMPAIGN`)

Marketing campaign reference dimension for ROI attribution

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| CAMPAIGN_KEY | NUMBER(38,0) | campaign_key | Campaign Key | Surrogate key that uniquely identifies a campaign record. |
| CAMPAIGN_ID | VARCHAR(20) | campaign_id | Campaign ID | Business/natural identifier for the campaign from the source system. |
| CAMPAIGN_NAME | VARCHAR(200) | campaign_name | Campaign Name | Human-readable name of the campaign. |
| CAMPAIGN_TYPE | VARCHAR(50) | campaign_type | Campaign Type | Classification of campaign type (e.g., brand, performance, seasonal). |
| MEDIA_MIX | VARCHAR(100) | media_mix | Media Mix | Summary of channels/media included in the campaign. |
| BRAND | VARCHAR(100) | brand | Brand | Brand associated with the campaign. |
| OBJECTIVE | VARCHAR(100) | objective | Objective | Primary objective of the campaign. |
| TARGET_SEGMENT | VARCHAR(100) | target_segment | Target Segment | Intended customer/market segment targeted by the campaign. |
| START_DATE | DATE | start_date | Start Date | Campaign start date. |
| END_DATE | DATE | end_date | End Date | Campaign end date. |
| PLANNED_BUDGET | NUMBER(14,2) | planned_budget | Planned Budget | Budget planned for the campaign, in the specified currency. |
| ACTUAL_SPEND | NUMBER(14,2) | actual_spend | Actual Spend | Actual spend incurred for the campaign, in the specified currency. |
| CURRENCY | VARCHAR(3) | currency | Currency | ISO currency code for campaign financial amounts. |
| AGENCY | VARCHAR(100) | agency | Agency | Agency responsible for executing or managing the campaign. |
| CAMPAIGN_MANAGER | VARCHAR(100) | campaign_manager | Campaign Manager | Person responsible for managing the campaign. |
| GEO_SCOPE | VARCHAR(100) | geo_scope | Geographic Scope | Geographic coverage for the campaign. |
| STATUS | VARCHAR(20) | status | Status | Lifecycle status of the campaign. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |

## Customer Dimension (`RETAIL_DWH.CORE.DIM_CUSTOMER`)

Customer master dimension with SCD Type 2 history tracking

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| CUSTOMER_KEY | NUMBER(38,0) | customer_key | Customer Key | Surrogate key that uniquely identifies a customer dimension record (version). |
| CUSTOMER_ID | VARCHAR(20) | customer_id | Customer ID | Business/natural identifier for the customer from the source system. |
| FIRST_NAME | VARCHAR(100) | first_name | First Name | Customer first/given name. |
| LAST_NAME | VARCHAR(100) | last_name | Last Name | Customer last/family name. |
| FULL_NAME | VARCHAR(200) | full_name | Full Name | Customer full name. |
| EMAIL | VARCHAR(200) | email | Email | Customer email address. |
| PHONE | VARCHAR(30) | phone | Phone | Customer phone number. |
| GENDER | VARCHAR(10) | gender | Gender | Customer gender value as provided by the source. |
| DATE_OF_BIRTH | DATE | date_of_birth | Date of Birth | Customer date of birth. |
| AGE_BAND | VARCHAR(20) | age_band | Age Band | Age grouping/band for the customer. |
| LOYALTY_TIER | VARCHAR(20) | loyalty_tier | Loyalty Tier | Customer loyalty program tier. |
| LOYALTY_POINTS | NUMBER(38,0) | loyalty_points | Loyalty Points | Customer loyalty points balance. |
| CUSTOMER_SEGMENT | VARCHAR(50) | customer_segment | Customer Segment | Assigned customer segment used for analytics/marketing. |
| ACQUISITION_CHANNEL | VARCHAR(50) | acquisition_channel | Acquisition Channel | Channel through which the customer was acquired. |
| ACQUISITION_DATE | DATE | acquisition_date | Acquisition Date | Date the customer was acquired. |
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key referencing the customer's geography. |
| IS_ACTIVE | BOOLEAN | is_active | Is Active | Indicates whether the customer is active. |
| IS_NEWSLETTER | BOOLEAN | is_newsletter | Is Newsletter Subscribed | Indicates whether the customer is subscribed to newsletters. |
| PREFERRED_LANGUAGE | VARCHAR(10) | preferred_language | Preferred Language | Customer preferred language code. |
| LIFETIME_VALUE_BAND | VARCHAR(20) | lifetime_value_band | Lifetime Value Band | Customer lifetime value grouping/band. |
| EFF_START_DATE | DATE | eff_start_date | Effective Start Date | SCD Type 2 effective start date for this customer record version. |
| EFF_END_DATE | DATE | eff_end_date | Effective End Date | SCD Type 2 effective end date for this customer record version. |
| IS_CURRENT | BOOLEAN | is_current | Is Current | Indicates whether this record is the current SCD version. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |
| UPDATED_AT | TIMESTAMP_NTZ(9) | updated_at | Updated At | Timestamp when the record was last updated. |
