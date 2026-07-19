# Continuing the Refactoring

## Overview

After completing the `fact_sales` table, I continued refactoring the remaining tables in the semantic model.

During this phase, I focused on building additional fact and dimension tables, integrating them with the existing model, and improving the overall star schema.

---

## Building the Inventory Fact

The inventory data contains the planned inventory units for each product on a monthly basis. Since the table stores measurable business data over time, I modelled it as a fact table.

To prepare the `fact_inventory` table, I:

- Promoted the first row as column headers.
- Unpivoted the monthly inventory columns into rows so that each record represents the inventory units for a single product and month.
- Changed the `month` column data type to Date.
- Merged the `dim_products` table to retrieve the `product_key`.
- Expanded the `product_key` column from the merged table.
- Removed the `product_name` column after replacing it with the `product_key`.
- Renamed the columns to follow the project's modeling standards and improve consistency.
- Reordered the columns to improve readability and maintain a consistent column layout.

The completed Power Query transformation is shown below.

![Fact Inventory Power Query](../images/fact_inventory_power_query.png)

---

## Updating the Semantic Model

After creating the `fact_inventory` table, I connected it to the existing `dim_products` table using the `product_key`.

The updated semantic model is shown below.

![Model After Inventory](../images/model_after_inventory.png)

---

## Summary

The semantic model now includes an additional fact table for inventory data. By reusing the existing product dimension, the model remains consistent and avoids unnecessary duplication.

---

## What's Next

The next step is to continue refactoring the remaining transaction tables, build additional fact and dimension tables where required, and further refine the semantic model.
