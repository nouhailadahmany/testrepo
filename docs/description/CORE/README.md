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


## Date Dimension (`RETAIL_DWH.CORE.DIM_DATE`)

Conformed time dimension covering 2020–2026

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| DATE_KEY | NUMBER(38,0) | date_key | Date Key | Surrogate key representing the date (typically in YYYYMMDD form). |
| FULL_DATE | DATE | full_date | Full Date | Calendar date. |
| DAY_OF_WEEK | NUMBER(38,0) | day_of_week | Day of Week Number | Numeric day of week for the date. |
| DAY_NAME | VARCHAR(10) | day_name | Day Name | Name of the day of week (e.g., Monday). |
| DAY_OF_MONTH | NUMBER(38,0) | day_of_month | Day of Month | Day of month (1–31). |
| DAY_OF_YEAR | NUMBER(38,0) | day_of_year | Day of Year | Day number within the year (1–365/366). |
| WEEK_OF_YEAR | NUMBER(38,0) | week_of_year | Week of Year | Week number within the year. |
| MONTH_NUMBER | NUMBER(38,0) | month_number | Month Number | Month number (1–12). |
| MONTH_NAME | VARCHAR(10) | month_name | Month Name | Full month name (e.g., January). |
| MONTH_SHORT | VARCHAR(3) | month_short | Month Abbreviation | Short month name (e.g., Jan). |
| QUARTER | NUMBER(38,0) | quarter | Quarter Number | Quarter number (1–4). |
| QUARTER_NAME | VARCHAR(6) | quarter_name | Quarter Name | Quarter label (e.g., Q1). |
| YEAR | NUMBER(38,0) | year | Year | Calendar year. |
| IS_WEEKEND | BOOLEAN | is_weekend | Is Weekend | Indicates whether the date falls on a weekend. |
| IS_HOLIDAY | BOOLEAN | is_holiday | Is Holiday | Indicates whether the date is a holiday. |
| HOLIDAY_NAME | VARCHAR(100) | holiday_name | Holiday Name | Name of the holiday, when applicable. |
| FISCAL_YEAR | NUMBER(38,0) | fiscal_year | Fiscal Year | Fiscal year corresponding to the date. |
| FISCAL_QUARTER | NUMBER(38,0) | fiscal_quarter | Fiscal Quarter | Fiscal quarter corresponding to the date. |
| FISCAL_MONTH | NUMBER(38,0) | fiscal_month | Fiscal Month | Fiscal month corresponding to the date. |
| SEASON | VARCHAR(10) | season | Season | Season label for the date (e.g., Spring/Summer). |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |

## Geography Dimension (`RETAIL_DWH.CORE.DIM_GEOGRAPHY`)

Geographic reference dimension for all regional analysis

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key that uniquely identifies a geography record. |
| COUNTRY_CODE | VARCHAR(3) | country_code | Country Code | Country code for the geography (typically ISO). |
| COUNTRY_NAME | VARCHAR(100) | country_name | Country Name | Country name for the geography. |
| REGION | VARCHAR(100) | region | Region | Top-level region grouping for the geography. |
| SUB_REGION | VARCHAR(100) | sub_region | Sub-Region | Sub-region grouping for the geography. |
| STATE_PROVINCE | VARCHAR(100) | state_province | State/Province | State or province within the country. |
| CITY | VARCHAR(100) | city | City | City name. |
| POSTAL_CODE | VARCHAR(20) | postal_code | Postal Code | Postal/ZIP code. |
| LATITUDE | FLOAT | latitude | Latitude | Latitude coordinate for the geography. |
| LONGITUDE | FLOAT | longitude | Longitude | Longitude coordinate for the geography. |
| TIME_ZONE | VARCHAR(50) | time_zone | Time Zone | Time zone identifier for the geography. |
| CURRENCY_CODE | VARCHAR(3) | currency_code | Currency Code | Currency code associated with the geography. |
| CURRENCY_NAME | VARCHAR(50) | currency_name | Currency Name | Currency name associated with the geography. |
| IS_EU_MEMBER | BOOLEAN | is_eu_member | Is EU Member | Indicates whether the country is a member of the European Union. |
| POPULATION_BAND | VARCHAR(20) | population_band | Population Band | Population size grouping/band for the geography. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |
| UPDATED_AT | TIMESTAMP_NTZ(9) | updated_at | Updated At | Timestamp when the record was last updated. |
