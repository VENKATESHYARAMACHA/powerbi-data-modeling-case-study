# Prepare and Explore

## Overview

Before making any changes to the semantic model, I spent some time exploring the existing data model.

Instead of immediately renaming tables or deleting columns, I wanted to understand how the business works, what data was available, and how the tables were connected. This helped me make informed decisions during the cleanup process.

---

## The Rule

> **Understand the data before you change anything.**

The more time I spent exploring the model, the easier it became to identify issues and avoid mistakes during the refactoring process.

---

## What I Wanted to Understand

During this phase, I focused on answering a few important questions:

- What is the business?
- What are the main business entities?
- Which tables are dimensions?
- Which tables are facts?

Having answers to these questions gave me a clear direction before starting the refactoring.

---

## Exploring the Existing Model

I reviewed every table in the semantic model to understand its purpose.

From the exploration, I found several descriptive tables that could become **dimension tables**, including:

- Customers
- Products
- Addresses
- Cities
- Regions
- Subcategories

These tables mainly contained descriptive attributes that provide business context.

I also identified several transactional tables that could become **fact tables**, such as:

- Orders
- Order Line Items
- Invoices
- Invoice Lines
- Payments
- Shipments
- Campaign Logs

These tables contained business events with dates, quantities, and amounts, making them suitable for fact tables.

---

## Issues I Identified

While reviewing the model, I found several areas that required cleanup.

Some of the issues included:

- Duplicate tables containing the same data.
- Orders stored in separate yearly tables.
- Tables with unclear or meaningless names.
- Technical columns that were not useful for reporting.
- Repeated business information across multiple tables.
- Inconsistent naming conventions.

Identifying these problems early helped me plan the refactoring process.

---

## Preparing Power Query

Before creating new tables, I organized the Power Query editor to keep the project structured.

I created the following folders:

- **Stage** – Original source tables
- **Dimensions** – Clean dimension tables
- **Facts** – Clean fact tables
- **Support** – Helper and supporting tables

This made it much easier to manage the queries as the project progressed.

---

## Summary

After completing this phase, I had a much better understanding of the semantic model.

I was able to:

- Understand the business domain.
- Identify the main business entities.
- Separate potential dimensions from facts.
- Spot data quality issues.
- Organize the Power Query environment for the upcoming refactoring work.

This preparation gave me a solid foundation before modifying the semantic model.

---

## What's Next

Now that I understand the existing model, the next step is to clean and standardize the dimension tables.

➡️ Continue to [04_dimensions.md](04_dimensions.md)
