# Cleaning Log

## Issues Found
- Extra leading/trailing spaces in text fields.
- Inconsistent text formatting across multiple columns.
- Missing values in the Region column (25 records).
- Missing values in the Ship Mode column (21 records).
- Missing values in the Discount column (18 records).
- Duplicate records were present.
- Duplicate Order IDs with conflicting information were identified.
- Negative discount values were found.
- Ship dates earlier than order dates were identified.
- Mixed discount formats (decimal and percentage) were found.

## Cleaning Actions Performed
- Preserved the original dataset as `raw_orders.xlsx`.
- Created a separate cleaned dataset (`cleaned_orders.xlsx`).
- Trimmed extra spaces and standardized text formatting.
- Standardized date formats for Order Date and Ship Date.
- Calculated Shipping Delay Days.
- Removed exact duplicate rows.
- Filled missing Region values with "Unknown".
- Filled missing Ship Mode values with "Unknown".
- Replaced valid missing Discount values with 0.
- Created calculated columns including cleaned_discount, calculated_sales, calculated_profit, profit_margin, order_month, order_year, shipping_delay_days, and data_quality_flag.

## Business Rules Applied
- Missing Region → Replaced with "Unknown".
- Missing Ship Mode → Replaced with "Unknown".
- Missing Discount → Replaced with 0 where applicable.
- Negative Discounts → Flagged as Invalid.
- Ship Date earlier than Order Date → Flagged as Invalid.
- Cancelled and Failed orders were excluded from completed sales summaries.
- Refunded orders were summarized separately.

## Assumptions Made
- Valid discount range was assumed to be 0–100%.
- Mixed discount formats were standardized.
- Profit margin was calculated using calculated sales and calculated profit.

## Records Removed
- 20 exact duplicate records were removed.

## Records Flagged
- Duplicate Order IDs requiring review were flagged.
- Invalid shipping records were flagged.
- Records with missing Region or Ship Mode were marked as Warning.
- Records with invalid discounts were marked as Invalid.

## Limitations
- Business rules were applied based on the provided assignment instructions.
- Some business assumptions were required because the dataset contained mixed discount formats.