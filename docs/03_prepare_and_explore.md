# Prepare and Explore

## Overview

Before making any changes to the semantic model, I explored all the tables to understand the business and how the data was organized.

The objective of this phase was not to clean the model immediately, but to identify the main business entities, understand the purpose of each table, and determine which tables would eventually become dimensions or facts.

---

## Understanding the Existing Model

I reviewed each table in the model to understand what information it contained.

Some tables represented business entities such as:

- Addresses
- Customers
- Products
- Regions
- Cities
- Subcategories

These tables mainly contained descriptive information, making them good candidates for **dimension tables**.

Other tables represented business events such as:

- Orders
- Order Line Items
- Invoices
- Invoice Lines
- Payments
- Shipments
- Campaign Logs

These tables contained transactional data with dates, quantities, amounts, and other measurable values, making them suitable candidates for **fact tables**.

---

## Issues Identified During Exploration

While exploring the model, I found several issues that would need to be addressed during the refactoring process.

Some examples included:

- Duplicate shipment tables (`Shipments` and `Sheet1`)
- Orders split across multiple yearly tables
- A table (`Dimension Order`) containing only IDs with no useful business context
- Inconsistent naming conventions across tables
- Technical columns such as hash keys and source IDs
- Repeated customer and location information in multiple tables

These observations helped me identify which tables could be cleaned, merged, renamed, or removed later.

---

## Preparing Power Query

Before starting the refactoring, I organized the queries in Power Query into separate folders to make the project easier to manage.

The folders I created were:

- **Stage** – Original source tables
- **Dimensions** – Dimension tables created during the cleanup
- **Facts** – Fact tables created during the cleanup
- **Support** – Supporting tables such as security or helper tables

Keeping the queries organized from the beginning makes it easier to track changes as the model grows.

---

## Summary

After exploring the model, I had a clear understanding of:

- The business entities
- The transactional tables
- Potential dimension and fact tables
- Existing data quality issues
- Areas that required cleanup before building a proper star schema

This exploration gave me the confidence to begin refactoring the semantic model while following the modeling standards defined earlier.

---

## What's Next

The next step is to start cleaning and standardizing the dimension tables.

➡️ Continue to [04_dimensions.md](04_dimensions.md)
