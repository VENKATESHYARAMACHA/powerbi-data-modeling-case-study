# Modeling Standards

## Overview

Before making any changes, it is important to define a consistent set of modeling standards.

These standards will be followed throughout the project to keep the semantic model clean, readable, and easier to maintain. Every table, column, and relationship will be updated based on these rules.

---

## Naming Convention

All table and column names will follow the **snake_case** naming convention.

### Examples

| ❌ Avoid | ✅ Use |
|----------|--------|
| CustomerName | customer_name |
| OrderDate | order_date |
| Total-Sales | total_sales |
| ShipCountry | ship_country |

---

## Table Naming

Fact tables will use the `fact_` prefix, and dimension tables will use the `dim_` prefix.

### Examples

| ❌ Avoid | ✅ Use |
|----------|--------|
| sales | fact_sales |
| inventory | fact_inventory |
| customer | dim_customer |
| product_dimension | dim_product |

---

## Key Naming

Source system keys will end with `_id`.

Surrogate keys created during modeling will end with `_key`.

### Examples

| ❌ Avoid | ✅ Use |
|----------|--------|
| CustKey | customer_key |
| UID_Product | product_key |
| id_customer | customer_id |
| order_pk | order_id |

---

## Language

All table names and column names will be in **English**.

### Examples

| ❌ Avoid | ✅ Use |
|----------|--------|
| land | country |
| bestell_date | order_date |
| gesamt_sales | total_sales |
| kunden_name | customer_name |

---

## Friendly Names

Names should be easy to read and understand.

Avoid abbreviations unless they are widely accepted.

### Examples

| ❌ Avoid | ✅ Use |
|----------|--------|
| cust_nm | customer_name |
| tot_rev | total_revenue |
| ord_st_cd | order_status |
| shp_ctry | ship_country |

---

## Keep Only What Adds Value

The semantic model should only contain objects that support reporting and analysis.

During the cleanup, the following may be removed if they are not required:

- Technical columns
- Staging tables
- Duplicate tables
- Unused relationships
- Unused columns

---

## Dimensional Modeling

The semantic model should follow dimensional modeling best practices.

- Business processes should be separated into individual fact tables.
- Dimension tables should contain descriptive business information and be shared wherever possible.
- Fact tables should connect to dimensions using keys.
- Shared (conformed) dimensions should be reused across multiple fact tables.
- Relationships should remain simple, consistent, and easy to understand.

This approach enables the semantic model to evolve from individual star schemas into a scalable Galaxy Schema (Fact Constellation) as additional business processes are added.

---

## Summary

The standards defined in this document will be followed throughout the project to create a clean, consistent, and maintainable semantic model.

---

## What's Next

The next step is to review the existing model and identify fact and dimension tables before starting the refactoring process.

➡️ Continue with [03_prepare_and_explore.md](03_prepare_and_explore.md)
