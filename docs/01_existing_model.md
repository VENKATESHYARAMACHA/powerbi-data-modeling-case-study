# Existing Semantic Model

## Overview

Before beginning the refactoring process, I wanted to get a high-level understanding of the existing semantic model.

This document captures my initial assessment of the model based on its overall structure. At this stage, I focused on identifying visible design issues rather than analyzing the underlying data.

---

## Existing Model

The image below shows the semantic model before any modifications.

![Existing Semantic Model](../images/existing_model.png)

---

## First Impression

At first glance, the semantic model appeared more complex than necessary.

Even without exploring the individual tables, I could see several structural issues that would make the model harder to understand and maintain over time.

---

## Initial Observations

### Inconsistent Naming

Different naming conventions were used across tables and columns, making the model less consistent and harder to navigate.

### Duplicate Data Structures

Some business entities appeared to be represented by multiple tables instead of a single logical structure.

### Technical Metadata

Several tables contained technical or system-generated columns that did not appear to add value to the semantic model.

### Complex Relationships

The relationship diagram contained many interconnected tables, making it difficult to understand the overall data model.

### Lack of Standardization

There was no clear and consistent approach for organizing tables, naming objects, or separating dimensions from facts.

---

## Refactoring Goal

Based on these initial observations, my goal is to improve the semantic model by:

- Applying consistent naming conventions
- Building a clear star schema
- Removing unnecessary tables and columns
- Simplifying relationships
- Improving readability and maintainability

The business logic and source data will remain unchanged throughout this project.

---

## What's Next

The next step is to define the modeling standards that will guide the refactoring process and ensure consistency across the semantic model.

Once those standards are established, I will explore the existing data in detail to understand the business entities, identify potential dimension and fact tables, and plan the refactoring before making any structural changes.

➡️ Continue with [02_modeling_standards.md](02_modeling_standards.md)
