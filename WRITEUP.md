# Homework 2 Write-Up

## Task 0: Initial Data Inspection

I first inspected the shape, first few rows, and tidiness of all three datasets. The revenue dataset had 5 rows and 13 columns and was not tidy because quarter values were stored as separate columns. This violates the rule that each variable should have its own column and causes multiple company-quarter observations to be stored in one row. The orders dataset was tidy because each row represented one order, while the shipments dataset was tidy because each row represented one shipment. My initial visualization was a bar chart of company revenue for 2023-Q1.

## Task 1: Tidying Revenue

The revenue dataset was in wide format. I reshaped it into long format with `company`, `quarter`, and `revenue` columns. After reshaping, each row represents one company-quarter observation. This fixes the tidy-data problem because quarter is now a variable stored in its own column rather than being spread across multiple column names.

## Task 2: Checking Keys

I checked `order_id` before joining the orders and shipments datasets. `order_id` was unique in the orders table but not unique in shipments. This shows that the relationship is one-to-many because one order can have multiple shipments. Therefore, I expected some order rows to repeat after the join.

## Task 3: Orders and Shipments

I joined orders and shipments using `order_id`. I used a left join because the analysis focuses on mean order amount per customer, so all orders should be preserved even if an order does not have a shipment. The mean calculated from the joined table can be different because orders with multiple shipments appear multiple times. The mean calculated directly from the orders table is therefore correct because each order is counted once.

## Task 4: Analysis-Ready Table

I combined the joined order/shipment data with the tidy revenue data using `company` and `quarter`. These two variables identify the correct revenue for a company during a particular quarter. I preserved the order/shipment observations and added the matching revenue. I also reset the index so the final table did not contain leftover index artifacts.

## Task 5: Visualization

My Step 0 visualization required manually selecting the `2023-Q1` column because each quarter was stored separately. For the final visualization, I removed repeated company-quarter revenue values caused by the one-to-many order/shipment join and calculated average revenue by company. Tidying the revenue data made it easier to work with multiple quarters without manually selecting individual quarter columns.
