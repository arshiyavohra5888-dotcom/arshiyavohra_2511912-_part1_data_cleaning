# Retail Sales Data Cleaning and Analysis

## Problem Summary

This project focuses on cleaning and validating a retail sales dataset containing issues such as inconsistent text formatting, mixed date formats, missing values, duplicate records, invalid discounts, and business rule violations. The objective was to prepare a clean, analysis-ready dataset and generate business reports.

## Dataset Description

The dataset contains order-level retail sales information, including:

* Order details
* Customer details
* Product details
* Region and location
* Sales, cost, and profit
* Discounts
* Payment status
* Order status
* Shipping information

## Tools Used

* WPS Office Spreadsheet
* Microsoft Excel compatible functions
* Pivot Tables
* Basic formulas (IF, TRIM, etc.)
* Filters and Find & Replace

## Cleaning Steps Performed

1. Standardized text fields.
2. Removed extra spaces.
3. Corrected inconsistent capitalization.
4. Standardized date formats.
5. Created `shipping_delay_days`.
6. Filled missing Region values with **Unknown**.
7. Filled missing Ship Mode values with **Unknown**.
8. Filled missing Discount values with **0**.
9. Identified duplicate records.
10. Created calculated columns:

* `shipping_delay_days`
* `profit_margin_pct`
* `data_quality_flag`

## Business Rules Applied

* Missing Region → Filled with **Unknown**
* Missing Ship Mode → Filled with **Unknown**
* Missing Discount → Filled with **0**
* Negative Discounts → Flagged as Invalid
* Discounts greater than 50% → Flagged as Invalid
* Cancelled Orders → Excluded from completed sales summary
* Failed Payments → Excluded from completed sales summary
* Refunded Orders → Reported separately
* Ship Date before Order Date → Flagged as invalid shipping record

## Summary of Data Quality Issues Found

* Missing Region: **26**
* Missing Ship Mode: **22**
* Missing Discount: **18**
* Negative Discounts: **16**
* Discounts above 50%: **3**
* Cancelled Orders: **146**
* Failed Payments: **69**
* Refunded Orders: **72**
* Ship Date before Order Date: **37**
* Exact Duplicate Rows: **20**

## Summary of Pivot Reports

The following Pivot Tables were created:

1. Sales and Profit by Region
2. Sales and Profit by Category and Sub-category
3. Order Count by Ship Mode
4. Profit Margin by Customer Segment
5. Order Status by Region
6. Monthly Sales Trend

## Key Business Insights

* Most revenue comes from a limited number of regions.
* Several records contained invalid or unusually high discounts.
* Missing data was minimal and successfully handled.
* Cancelled and failed transactions were excluded from completed sales analysis.
* Refunded orders were reported separately for better business tracking.

## Assumptions and Limitations

### Assumptions

* Missing discounts were treated as 0.
* Missing Region and Ship Mode values were replaced with "Unknown".

### Limitations

* Some mixed date formats required manual verification.
* Invalid records were flagged instead of automatically corrected.

## Screenshots Included

* Raw dataset preview
* Cleaned dataset preview
* Pivot Summary 1
* Pivot Summary 2
