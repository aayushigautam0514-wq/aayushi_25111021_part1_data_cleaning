# Part 1: Data Cleaning and Validation

## Problem Summary

This project focuses on cleaning and validating a retail sales dataset containing inconsistent text formatting, mixed date formats, duplicate records, missing values, invalid discounts, and calculation mismatches. The objective was to prepare a clean, validated, and analysis-ready dataset.

## Dataset Description

The dataset contains retail order-level information, including:

* Customer details
* Product details
* Order and shipping information
* Sales, cost, and profit
* Discount
* Payment status
* Order status

## Tools Used

* Microsoft Excel
* Excel Functions (TRIM, DATEVALUE, IF, TEXT, YEAR, ROUND, COUNTIF)
* Pivot Tables
* Conditional Formatting

## Cleaning Steps Performed

* Preserved the original dataset separately.
* Cleaned text fields and removed extra spaces.
* Standardized date formats.
* Removed exact duplicate records.
* Identified duplicate Order IDs.
* Filled missing Region and Ship Mode values with "Unknown".
* Standardized discount values.
* Created calculated columns including cleaned discount, calculated sales, calculated profit, profit margin, shipping delay days, order month, order year, and data quality flag.

## Business Rules Applied

* Missing Region → Filled with "Unknown".
* Missing Ship Mode → Filled with "Unknown".
* Missing Discount → Replaced with 0 where applicable.
* Negative Discount → Flagged as Invalid.
* Ship Date earlier than Order Date → Flagged as Invalid.
* Cancelled and Failed orders were excluded from completed sales summaries.
* Refunded orders were summarized separately.

## Summary of Data Quality Issues Found

* Missing Region values
* Missing Ship Mode values
* Missing Discount values
* Duplicate records
* Duplicate Order IDs
* Negative discounts
* Invalid shipping records
* Mixed discount formats

## Summary of Final Pivot Reports

* Sales and Profit by Region
* Sales and Profit by Category and Sub-category
* Order Count by Ship Mode
* Profit Margin by Customer Segment
* Refunded/Cancelled/Failed Orders by Region
* Monthly Sales Trend

## Key Business Insights

* Regional sales performance varies significantly.
* Product categories contribute differently to profit.
* Standard Class is the most frequently used shipping mode.
* Customer segments show different profit margins.
* Cancelled, refunded, and failed orders should be monitored separately.

## Assumptions and Limitations

### Assumptions

* Discounts were standardized before calculations.
* Missing Region and Ship Mode values were replaced with "Unknown".
* Business rules provided in the assignment were followed.

### Limitations

* Data cleaning was limited to the business rules provided.
* Some assumptions were necessary due to inconsistent source data.

## Screenshots Included

* Raw dataset preview
* Cleaned dataset preview
* Pivot Summary 1
* Pivot Summary 2
