# Cleaning Log

## 1. Issues Found

* Missing region values
* Missing ship mode values
* Missing discount values
* Negative discount values
* Discount values greater than 50%
* Duplicate rows
* Duplicate order IDs
* Ship dates earlier than order dates
* Inconsistent text formatting
* Mixed date formats

## 2. Cleaning Actions Performed

* Standardized text fields using proper formatting.
* Filled missing region values with "Unknown".
* Filled missing ship mode values with "Unknown".
* Filled missing discount values with 0.
* Standardized date formats.
* Created shipping_delay_days column.
* Created profit_margin_pct column.
* Created data_quality_flag column.
* Identified duplicate records.

## 3. Business Rules Applied

* Missing region → Filled with "Unknown".
* Missing ship mode → Filled with "Unknown".
* Missing discount → Filled with 0.
* Negative discounts → Flagged as invalid.
* Discounts above 50% → Flagged as invalid.
* Cancelled orders excluded from completed sales summary.
* Failed payments excluded from completed sales summary.
* Refunded orders summarized separately.
* Ship dates before order dates flagged as invalid shipping records.

## 4. Assumptions Made

* Missing discount values were treated as 0.
* Missing region and ship mode values were replaced with "Unknown".
* Duplicate records were retained for review unless they were exact duplicates.

## 5. Records Removed

* Exact duplicate rows removed: 20
* Conflicting duplicate records: Flagged for review

## 6. Records Flagged

* Negative discounts: 16
* Discounts above 50%: 3
* Invalid shipping records: 37
* Duplicate records: Flagged

## 7. Limitations

* Some date formats required manual validation.
* Certain invalid records were flagged instead of corrected automatically.
