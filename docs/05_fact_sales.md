# Building the Sales Fact Table

## Overview

With the core dimension tables in place, the next step was to build the first fact table for the semantic model.

Instead of loading the transaction tables directly into the model, I transformed them into a clean fact table by replacing descriptive attributes with dimension keys, removing redundant columns, and extracting additional dimensions wherever required.

The objective of this phase was to create a well-structured fact table that stores the business measures while using keys to connect with the dimension tables.

---

## Understanding the Transaction Data

Before building the fact table, I reviewed the sales-related transaction tables to understand their structure and level of detail.

This helped me identify the columns that should remain as business measures and the descriptive attributes that should be replaced with dimension keys.

---
## Choosing the Fact Table

Before creating the fact table, I analysed the sales transaction tables to determine which one should become the primary fact table.

The `orders_2025` and `orders_2026` tables contain order-level information, where each row represents a complete order. In contrast, the `order_line_items` table stores individual products within each order, along with the business measures such as quantity, price, cost, and line total.

Since the business measures are recorded at the order line level, I chose the `order_line_items` table as the foundation for the `fact_sales` table. The orders tables were then used to provide additional order information during the transformation process.

---
## Building the Sales Fact

I created the `fact_sales` table by transforming the sales transaction data and integrating it with the dimension tables created during the previous phase.

During this process, I:

- Appended the `orders_2025` and `orders_2026` tables to create a single orders table.
- Merged the orders table into the `fact_sales` table to retrieve the required order information.
- Replaced customer attributes with the `customer_id`.
- Replaced product attributes with the `product_key`.
- Created the `dim_order_flag` dimension and added the `flag_key`.
- Created the `dim_geo` dimension and added the `ship_to_geo_key` and `bill_to_geo_key`.
- Removed descriptive columns after replacing them with the corresponding dimension keys.
- Renamed the columns to follow the project's naming standards.
- Reordered the columns to improve readability.

The completed Power Query transformation is shown below.

![Fact Sales Power Query](../images/fact_sales_power_query.png)

---

## Updating the Semantic Model

After completing the `fact_sales` table, I connected it with the dimension tables using their respective keys.

At this stage, the semantic model started taking the shape of a star schema, with the fact table connected to the dimensions built so far.

The updated semantic model is shown below.

![Model After Fact Sales](../images/data_model_after_fact_sales.png)

---

## Summary

By the end of this phase, I had completed the first fact table and connected it to the existing dimensions using their respective keys.

This reduced data redundancy, improved the overall structure of the semantic model, and established a solid foundation for continuing the refactoring process.

---

## What's Next

With the first fact table completed, the next step is to continue refactoring the remaining transaction tables, extract additional dimensions wherever required, and complete the semantic model.

➡️ Continue to [06_remaining_dimensions.md](06_continuing_refactoring.md)
