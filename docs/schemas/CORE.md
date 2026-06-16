# Schema: CORE

## Summary
- Tables: 10
- Columns: 223
- Constraints present: true
- Notes: TABLE_CONSTRAINTS + REFERENTIAL_CONSTRAINTS returned; KEY_COLUMN_USAGE not accessible so FK column-level mappings are inferred via naming.

## Table classification
| Table | Type | Classification | Confidence | Key candidates | Notes |
|---|---|---|---|---|---|
| DIM_CAMPAIGN | BASE TABLE | DIMENSION | high | CAMPAIGN_KEY | Declared PK present. |
| DIM_CUSTOMER | BASE TABLE | DIMENSION | high | CUSTOMER_KEY | SCD-like columns (EFF_START_DATE, EFF_END_DATE, IS_CURRENT). |
| DIM_DATE | BASE TABLE | DIMENSION | high | DATE_KEY | Calendar dimension. |
| DIM_GEOGRAPHY | BASE TABLE | DIMENSION | high | GEO_KEY | Geography dimension. |
| DIM_PRODUCT | BASE TABLE | DIMENSION | high | PRODUCT_KEY | Product dimension. |
| DIM_PROMOTION | BASE TABLE | DIMENSION | high | PROMO_KEY | Promotion dimension. |
| DIM_STORE | BASE TABLE | DIMENSION | high | STORE_KEY | Store dimension. |
| FACT_CAMPAIGN_PERFORMANCE | BASE TABLE | FACT | high | PERF_KEY | Many metrics + multiple dimension keys. |
| FACT_INVENTORY | BASE TABLE | FACT | high | INVENTORY_KEY | Inventory measures + multiple dimension keys. |
| FACT_SALES | BASE TABLE | FACT | high | SALE_KEY | Sales measures + multiple dimension keys; has return fields. |

## Relationships
| From table | From columns | To table | To columns | Type | Confidence | Basis |
|---|---|---|---|---|---|---|
| DIM_CUSTOMER | GEO_KEY | DIM_GEOGRAPHY | GEO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming (KEY_COLUMN_USAGE unavailable). |
| DIM_STORE | GEO_KEY | DIM_GEOGRAPHY | GEO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| DIM_PROMOTION | CAMPAIGN_KEY | DIM_CAMPAIGN | CAMPAIGN_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | DATE_KEY | DIM_DATE | DATE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | RETURN_DATE_KEY | DIM_DATE | DATE_KEY | many-to-one | low | Role-playing date key inferred by naming. |
| FACT_SALES | CUSTOMER_KEY | DIM_CUSTOMER | CUSTOMER_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | PRODUCT_KEY | DIM_PRODUCT | PRODUCT_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | STORE_KEY | DIM_STORE | STORE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | GEO_KEY | DIM_GEOGRAPHY | GEO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | CAMPAIGN_KEY | DIM_CAMPAIGN | CAMPAIGN_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_SALES | PROMO_KEY | DIM_PROMOTION | PROMO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_INVENTORY | DATE_KEY | DIM_DATE | DATE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_INVENTORY | PRODUCT_KEY | DIM_PRODUCT | PRODUCT_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_INVENTORY | STORE_KEY | DIM_STORE | STORE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_INVENTORY | GEO_KEY | DIM_GEOGRAPHY | GEO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_CAMPAIGN_PERFORMANCE | DATE_KEY | DIM_DATE | DATE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_CAMPAIGN_PERFORMANCE | CAMPAIGN_KEY | DIM_CAMPAIGN | CAMPAIGN_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_CAMPAIGN_PERFORMANCE | STORE_KEY | DIM_STORE | STORE_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |
| FACT_CAMPAIGN_PERFORMANCE | GEO_KEY | DIM_GEOGRAPHY | GEO_KEY | many-to-one | medium | Declared FK exists; column mapping inferred from naming. |

## Transformation patterns
### keys
- DATE_KEY
- CUSTOMER_KEY
- PRODUCT_KEY
- STORE_KEY
- GEO_KEY
- CAMPAIGN_KEY
- PROMO_KEY

### date
- FULL_DATE
- START_DATE
- END_DATE
- OPENING_DATE
- CLOSING_DATE
- RETURN_DATE_KEY
- EFF_START_DATE
- EFF_END_DATE

### flags
- IS_ACTIVE
- IS_NEWSLETTER
- IS_CURRENT
- IS_WEEKEND
- IS_HOLIDAY
- IS_OUT_OF_STOCK
- IS_LOW_STOCK
- IS_RETURNED

### metrics
- QUANTITY
- DISCOUNT_AMOUNT
- NET_PRICE
- TOTAL_COST
- GROSS_MARGIN
- SPEND
- REVENUE_ATTRIBUTED
- ROAS
- CTR
- CVR
- CPC
- CPM
- CPA
- OPENING_STOCK
- CLOSING_STOCK
- STOCK_VALUE_COST
- STOCK_VALUE_RETAIL
