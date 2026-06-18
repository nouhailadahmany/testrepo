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


## Product Dimension (`RETAIL_DWH.CORE.DIM_PRODUCT`)

Product master dimension with full commercial and formulation attributes

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| PRODUCT_KEY | NUMBER(38,0) | product_key | Product Key | Surrogate key that uniquely identifies a product record. |
| PRODUCT_ID | VARCHAR(20) | product_id | Product ID | Business/natural identifier for the product from the source system. |
| PRODUCT_NAME | VARCHAR(200) | product_name | Product Name | Human-readable product name. |
| PRODUCT_SHORT_NAME | VARCHAR(100) | product_short_name | Product Short Name | Short/abbreviated name for the product. |
| BRAND | VARCHAR(100) | brand | Brand | Brand associated with the product. |
| CATEGORY_L1 | VARCHAR(100) | category_l1 | Category Level 1 | Top-level product category. |
| CATEGORY_L2 | VARCHAR(100) | category_l2 | Category Level 2 | Second-level product category. |
| CATEGORY_L3 | VARCHAR(100) | category_l3 | Category Level 3 | Third-level product category. |
| SKU | VARCHAR(50) | sku | SKU | Stock keeping unit identifier. |
| BARCODE | VARCHAR(50) | barcode | Barcode | Barcode/UPC/EAN value for the product. |
| UNIT_COST | NUMBER(12,4) | unit_cost | Unit Cost | Cost per unit in the specified currency. |
| UNIT_PRICE | NUMBER(12,4) | unit_price | Unit Price | List/standard selling price per unit in the specified currency. |
| GROSS_MARGIN_PCT | NUMBER(6,4) | gross_margin_pct | Gross Margin Percent | Gross margin percentage for the product. |
| CURRENCY | VARCHAR(3) | currency | Currency | ISO currency code for product financial amounts. |
| WEIGHT_GRAMS | NUMBER(38,0) | weight_grams | Weight (Grams) | Product weight in grams. |
| VOLUME_ML | NUMBER(38,0) | volume_ml | Volume (mL) | Product volume in milliliters. |
| SIZE_LABEL | VARCHAR(30) | size_label | Size Label | Human-readable size descriptor (e.g., 50ml, Large). |
| COLOR | VARCHAR(50) | color | Color | Color attribute of the product, when applicable. |
| FORMULATION_TYPE | VARCHAR(100) | formulation_type | Formulation Type | Formulation or product type classification. |
| TARGET_GENDER | VARCHAR(20) | target_gender | Target Gender | Intended target gender segment for the product. |
| TARGET_AGE_RANGE | VARCHAR(20) | target_age_range | Target Age Range | Intended target age range segment for the product. |
| KEY_INGREDIENTS | VARCHAR(500) | key_ingredients | Key Ingredients | Key ingredients or composition notes. |
| LAUNCH_DATE | DATE | launch_date | Launch Date | Product launch date. |
| DISCONTINUE_DATE | DATE | discontinue_date | Discontinue Date | Date the product was discontinued, if applicable. |
| IS_ACTIVE | BOOLEAN | is_active | Is Active | Indicates whether the product is active. |
| IS_HERO_PRODUCT | BOOLEAN | is_hero_product | Is Hero Product | Indicates whether the product is designated as a hero/key product. |
| SUSTAINABILITY_SCORE | NUMBER(4,2) | sustainability_score | Sustainability Score | Sustainability rating/score for the product. |
| COUNTRY_OF_ORIGIN | VARCHAR(3) | country_of_origin | Country of Origin | Country of origin code for the product. |
| SUPPLIER_ID | VARCHAR(20) | supplier_id | Supplier ID | Identifier of the supplier providing the product. |
| REORDER_POINT | NUMBER(38,0) | reorder_point | Reorder Point | Inventory level at which replenishment should be triggered. |
| REORDER_QUANTITY | NUMBER(38,0) | reorder_quantity | Reorder Quantity | Default quantity to reorder when replenishing inventory. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |
| UPDATED_AT | TIMESTAMP_NTZ(9) | updated_at | Updated At | Timestamp when the record was last updated. |

## Promotion Dimension (`RETAIL_DWH.CORE.DIM_PROMOTION`)

Promotion and discount dimension linked to marketing campaigns

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| PROMO_KEY | NUMBER(38,0) | promo_key | Promotion Key | Surrogate key that uniquely identifies a promotion record. |
| PROMO_ID | VARCHAR(20) | promo_id | Promotion ID | Business/natural identifier for the promotion from the source system. |
| PROMO_NAME | VARCHAR(200) | promo_name | Promotion Name | Human-readable name of the promotion. |
| PROMO_TYPE | VARCHAR(50) | promo_type | Promotion Type | Classification/type of promotion. |
| DISCOUNT_TYPE | VARCHAR(30) | discount_type | Discount Type | Type of discount (e.g., percent off, amount off). |
| DISCOUNT_VALUE | NUMBER(8,4) | discount_value | Discount Value | Discount value corresponding to the discount type. |
| MIN_PURCHASE_AMT | NUMBER(10,2) | min_purchase_amt | Minimum Purchase Amount | Minimum purchase amount required to qualify for the promotion. |
| MAX_DISCOUNT_AMT | NUMBER(10,2) | max_discount_amt | Maximum Discount Amount | Maximum discount amount allowed for the promotion. |
| START_DATE | DATE | start_date | Start Date | Promotion start date. |
| END_DATE | DATE | end_date | End Date | Promotion end date. |
| IS_STACKABLE | BOOLEAN | is_stackable | Is Stackable | Indicates whether the promotion can be combined with other promotions. |
| IS_LOYALTY_ONLY | BOOLEAN | is_loyalty_only | Is Loyalty Only | Indicates whether the promotion is restricted to loyalty members. |
| CAMPAIGN_KEY | NUMBER(38,0) | campaign_key | Campaign Key | Surrogate key referencing the related campaign, when applicable. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |


## Store Dimension (`RETAIL_DWH.CORE.DIM_STORE`)

Store and sales channel dimension for omnichannel reporting

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| STORE_KEY | NUMBER(38,0) | store_key | Store Key | Surrogate key that uniquely identifies a store record. |
| STORE_ID | VARCHAR(20) | store_id | Store ID | Business/natural identifier for the store from the source system. |
| STORE_NAME | VARCHAR(200) | store_name | Store Name | Human-readable store name. |
| STORE_TYPE | VARCHAR(50) | store_type | Store Type | Classification of store type (e.g., flagship, outlet). |
| CHANNEL | VARCHAR(50) | channel | Channel | Sales channel associated with the store (e.g., retail, online). |
| FORMAT | VARCHAR(50) | format | Format | Store format descriptor (e.g., small, large). |
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key referencing the store geography. |
| OPENING_DATE | DATE | opening_date | Opening Date | Date the store opened. |
| CLOSING_DATE | DATE | closing_date | Closing Date | Date the store closed, if applicable. |
| IS_ACTIVE | BOOLEAN | is_active | Is Active | Indicates whether the store is active. |
| FLOOR_AREA_SQM | NUMBER(38,0) | floor_area_sqm | Floor Area (Sqm) | Store floor area in square meters. |
| NUM_EMPLOYEES | NUMBER(38,0) | num_employees | Number of Employees | Number of employees working at the store. |
| MANAGER_NAME | VARCHAR(100) | manager_name | Manager Name | Name of the store manager. |
| PARTNER_NAME | VARCHAR(100) | partner_name | Partner Name | Name of the partner associated with the store, if applicable. |
| TIER | VARCHAR(20) | tier | Tier | Tier classification of the store (e.g., A/B/C). |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |

## Campaign Performance Fact (`RETAIL_DWH.CORE.FACT_CAMPAIGN_PERFORMANCE`)

Daily campaign performance metrics — grain: campaign × date × channel

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| PERF_KEY | NUMBER(38,0) | perf_key | Performance Key | Surrogate key that uniquely identifies a campaign performance fact record. |
| DATE_KEY | NUMBER(38,0) | date_key | Date Key | Surrogate key referencing the date of the performance record. |
| CAMPAIGN_KEY | NUMBER(38,0) | campaign_key | Campaign Key | Surrogate key referencing the campaign. |
| STORE_KEY | NUMBER(38,0) | store_key | Store Key | Surrogate key referencing the store/channel context, when applicable. |
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key referencing the geography context, when applicable. |
| IMPRESSIONS | NUMBER(38,0) | impressions | Impressions | Number of ad impressions. |
| REACH | NUMBER(38,0) | reach | Reach | Number of unique users reached. |
| CLICKS | NUMBER(38,0) | clicks | Clicks | Number of clicks. |
| VIDEO_VIEWS | NUMBER(38,0) | video_views | Video Views | Number of video views. |
| LIKES | NUMBER(38,0) | likes | Likes | Number of likes. |
| SHARES | NUMBER(38,0) | shares | Shares | Number of shares. |
| COMMENTS | NUMBER(38,0) | comments | Comments | Number of comments. |
| SAVES | NUMBER(38,0) | saves | Saves | Number of saves/bookmarks. |
| SESSIONS | NUMBER(38,0) | sessions | Sessions | Number of sessions attributed to the campaign. |
| ADD_TO_CARTS | NUMBER(38,0) | add_to_carts | Add to Carts | Number of add-to-cart events attributed to the campaign. |
| CHECKOUTS | NUMBER(38,0) | checkouts | Checkouts | Number of checkout events attributed to the campaign. |
| CONVERSIONS | NUMBER(38,0) | conversions | Conversions | Number of conversions attributed to the campaign. |
| SPEND | NUMBER(14,4) | spend | Spend | Advertising spend amount for the record grain. |
| REVENUE_ATTRIBUTED | NUMBER(14,4) | revenue_attributed | Revenue Attributed | Revenue attributed to the campaign for the record grain. |
| ROAS | NUMBER(10,4) | roas | ROAS | Return on ad spend for the record grain. |
| CTR | NUMBER(10,6) | ctr | CTR | Click-through rate for the record grain. |
| CVR | NUMBER(10,6) | cvr | CVR | Conversion rate for the record grain. |
| CPC | NUMBER(10,4) | cpc | CPC | Cost per click for the record grain. |
| CPM | NUMBER(10,4) | cpm | CPM | Cost per thousand impressions for the record grain. |
| CPA | NUMBER(10,4) | cpa | CPA | Cost per acquisition for the record grain. |
| CHANNEL_BREAKDOWN | VARCHAR(50) | channel_breakdown | Channel Breakdown | Channel or sub-channel identifier for the performance record. |
| CREATIVE_VERSION | VARCHAR(50) | creative_version | Creative Version | Creative variant/version identifier used for the campaign. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |


## Inventory Fact (`RETAIL_DWH.CORE.FACT_INVENTORY`)

Daily inventory snapshot — grain: product × store × date

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| INVENTORY_KEY | NUMBER(38,0) | inventory_key | Inventory Key | Surrogate key that uniquely identifies an inventory snapshot record. |
| DATE_KEY | NUMBER(38,0) | date_key | Date Key | Surrogate key referencing the snapshot date. |
| PRODUCT_KEY | NUMBER(38,0) | product_key | Product Key | Surrogate key referencing the product. |
| STORE_KEY | NUMBER(38,0) | store_key | Store Key | Surrogate key referencing the store. |
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key referencing the geography context for the snapshot. |
| OPENING_STOCK | NUMBER(38,0) | opening_stock | Opening Stock | Units on hand at the start of the day/snapshot period. |
| CLOSING_STOCK | NUMBER(38,0) | closing_stock | Closing Stock | Units on hand at the end of the day/snapshot period. |
| UNITS_RECEIVED | NUMBER(38,0) | units_received | Units Received | Units received into inventory during the period. |
| UNITS_SOLD | NUMBER(38,0) | units_sold | Units Sold | Units sold (inventory depletion) during the period. |
| UNITS_RETURNED | NUMBER(38,0) | units_returned | Units Returned | Units returned into inventory during the period. |
| UNITS_DAMAGED | NUMBER(38,0) | units_damaged | Units Damaged | Units marked as damaged during the period. |
| UNITS_WRITTEN_OFF | NUMBER(38,0) | units_written_off | Units Written Off | Units written off (e.g., shrinkage/expiration) during the period. |
| STOCK_VALUE_COST | NUMBER(14,4) | stock_value_cost | Stock Value (Cost) | Inventory value at cost for the snapshot/grain. |
| STOCK_VALUE_RETAIL | NUMBER(14,4) | stock_value_retail | Stock Value (Retail) | Inventory value at retail price for the snapshot/grain. |
| IS_OUT_OF_STOCK | BOOLEAN | is_out_of_stock | Is Out of Stock | Indicates whether the item is out of stock at the snapshot time. |
| IS_LOW_STOCK | BOOLEAN | is_low_stock | Is Low Stock | Indicates whether the item is below a low-stock threshold at the snapshot time. |
| DAYS_OF_SUPPLY | NUMBER(8,2) | days_of_supply | Days of Supply | Estimated number of days inventory will last based on expected demand. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |

## Sales Fact (`RETAIL_DWH.CORE.FACT_SALES`)

Core transactional sales fact table — grain: one row per order line

### Columns

| Column | Data type | Standardized name | Business name | Description |
|---|---|---|---|---|
| SALE_KEY | NUMBER(38,0) | sale_key | Sale Key | Surrogate key that uniquely identifies a sales order line record. |
| ORDER_ID | VARCHAR(30) | order_id | Order ID | Business identifier for the order. |
| ORDER_LINE_ID | VARCHAR(30) | order_line_id | Order Line ID | Business identifier for the order line. |
| DATE_KEY | NUMBER(38,0) | date_key | Date Key | Surrogate key referencing the order/sale date. |
| CUSTOMER_KEY | NUMBER(38,0) | customer_key | Customer Key | Surrogate key referencing the customer. |
| PRODUCT_KEY | NUMBER(38,0) | product_key | Product Key | Surrogate key referencing the product. |
| STORE_KEY | NUMBER(38,0) | store_key | Store Key | Surrogate key referencing the store/channel where the sale occurred. |
| GEO_KEY | NUMBER(38,0) | geo_key | Geography Key | Surrogate key referencing the geography context for the sale. |
| CAMPAIGN_KEY | NUMBER(38,0) | campaign_key | Campaign Key | Surrogate key referencing the attributed campaign, when applicable. |
| PROMO_KEY | NUMBER(38,0) | promo_key | Promotion Key | Surrogate key referencing the promotion applied, when applicable. |
| QUANTITY | NUMBER(38,0) | quantity | Quantity | Number of units sold on the order line. |
| UNIT_PRICE | NUMBER(12,4) | unit_price | Unit Price | Unit selling price for the order line in the transaction currency. |
| UNIT_COST | NUMBER(12,4) | unit_cost | Unit Cost | Unit cost for the product on the order line in the transaction currency. |
| GROSS_PRICE | NUMBER(14,4) | gross_price | Gross Price | Gross line amount before discounts and taxes, when populated. |
| DISCOUNT_AMOUNT | NUMBER(12,4) | discount_amount | Discount Amount | Discount amount applied to the order line. |
| NET_PRICE | NUMBER(14,4) | net_price | Net Price | Net line amount after discounts (and before or after tax depending on convention), when populated. |
| TOTAL_COST | NUMBER(14,4) | total_cost | Total Cost | Total cost for the line (typically unit cost × quantity), when populated. |
| GROSS_MARGIN | NUMBER(14,4) | gross_margin | Gross Margin | Gross margin amount for the order line, when populated. |
| TAX_RATE | NUMBER(6,4) | tax_rate | Tax Rate | Tax rate applied to the order line. |
| TAX_AMOUNT | NUMBER(12,4) | tax_amount | Tax Amount | Tax amount applied to the order line. |
| SHIPPING_COST | NUMBER(10,4) | shipping_cost | Shipping Cost | Shipping cost allocated to the order line, when applicable. |
| IS_RETURNED | BOOLEAN | is_returned | Is Returned | Indicates whether the order line was returned. |
| RETURN_DATE_KEY | NUMBER(38,0) | return_date_key | Return Date Key | Surrogate key referencing the return date, when applicable. |
| RETURN_REASON | VARCHAR(100) | return_reason | Return Reason | Reason provided for the return, when applicable. |
| LOYALTY_POINTS_EARNED | NUMBER(38,0) | loyalty_points_earned | Loyalty Points Earned | Loyalty points earned for the order line. |
| CURRENCY | VARCHAR(3) | currency | Currency | ISO currency code for transaction amounts. |
| FX_RATE_TO_EUR | NUMBER(10,6) | fx_rate_to_eur | FX Rate to EUR | Foreign exchange rate used to convert transaction currency to EUR. |
| NET_PRICE_EUR | NUMBER(14,4) | net_price_eur | Net Price (EUR) | Net line amount converted to EUR. |
| GROSS_MARGIN_EUR | NUMBER(14,4) | gross_margin_eur | Gross Margin (EUR) | Gross margin amount converted to EUR. |
| ORDER_SOURCE | VARCHAR(50) | order_source | Order Source | Source of the order (e.g., web, store, marketplace). |
| PAYMENT_METHOD | VARCHAR(50) | payment_method | Payment Method | Payment method used for the order. |
| FULFILLMENT_STATUS | VARCHAR(30) | fulfillment_status | Fulfillment Status | Fulfillment/delivery status of the order line. |
| CREATED_AT | TIMESTAMP_NTZ(9) | created_at | Created At | Timestamp when the record was created. |
