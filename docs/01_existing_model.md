# Existing Semantic Model

## Overview

This repository starts with an existing Power BI semantic model that has become difficult to maintain over time.

As more tables and data sources were added, the model lost consistency. Different naming conventions were used, duplicate tables were introduced, and the relationships became harder to understand.

The goal of this project is **not** to build reports or dashboards. The only objective is to clean and standardize the semantic model by following good data modeling practices.

---

## Existing Model

Below is the semantic model before making any changes.

![Existing Semantic Model](../images/existing_model.png)

---

## What I Found

Before making any changes, I spent some time understanding the existing model and noted a few areas that needed improvement.

### No Clear Star Schema

The model does not follow a proper star schema.

Instead of having a central fact table with related dimensions, many tables are connected together in a way that makes the model difficult to understand and maintain.

---

### Different Naming Styles

There is no single naming convention across the model.

Some examples:

| Current Name | Observation |
|--------------|-------------|
| `CUST_MASTER` | Uppercase |
| `Address` | PascalCase |
| `invoice_lines` | snake_case |
| `ORDERS_2025` | Year included in table name |

Using one consistent naming standard makes the model much easier to read.

---

### Duplicate Tables

Some business entities are split across multiple tables.

Example:

- `ORDERS_2025`
- `ORDERS_2026`

Instead of maintaining separate tables, these can be combined into a single table representing the same business process.

---

### Technical Columns

Some tables expose technical columns that are mainly useful during data loading but not for reporting or analysis.

Examples:

- `hash_key`
- `source_id`
- `_load_date`

These columns only add noise to the semantic model.

---

### Complex Relationships

The current relationship diagram is difficult to follow.

Some relationships make the model more complicated than necessary and reduce overall readability.

---

### Tables That Need Review

A few tables appear to be disconnected, staging-related, or no longer required in the semantic model.

These will be reviewed during the cleanup process.

---

## What This Project Will Do

During this project, I will:

- Apply consistent naming standards
- Separate facts and dimensions
- Simplify the relationship model
- Remove unnecessary tables and columns
- Make the semantic model easier to understand and maintain

The business logic will remain the same. The focus is only on improving the structure of the semantic model.

---

## What's Next

The next step is to define the modeling standards that will be followed throughout the project.

➡️ Continue with [02_modeling_standards.md](02_modeling_standards.md)
