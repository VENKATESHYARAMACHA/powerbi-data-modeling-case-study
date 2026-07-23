# Power BI Semantic Model Refactoring: From Legacy Model to Galaxy Schema

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Modeling-F2C811?logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Galaxy%20Schema-success)
![RLS](https://img.shields.io/badge/Security-Dynamic%20RLS-orange)
![Documentation](https://img.shields.io/badge/Documentation-Markdown-informational)

> An end-to-end Power BI semantic model refactoring project demonstrating dimensional modeling, semantic model optimization, reusable DAX measures, and Dynamic Row-Level Security (RLS).

---

# Overview

This repository documents my end-to-end journey of refactoring an existing Power BI semantic model into a clean, scalable, and enterprise-ready semantic model.

The original model contained duplicated tables, inconsistent naming conventions, unnecessary columns, and complex relationships. I analyzed the existing implementation and incrementally transformed it using dimensional modeling best practices.

The final solution follows a **Galaxy Schema (Fact Constellation)**.

---

# Project Objectives

- Analyze the existing semantic model.
- Apply dimensional modeling best practices.
- Create reusable dimensions.
- Build dedicated fact tables.
- Create a shared Date dimension.
- Develop reusable DAX measures.
- Implement Dynamic Row-Level Security.
- Improve scalability and maintainability.

---

# Development Process

## Phase 1 – Existing Model
Documentation: `docs/01_existing_model.md`

## Phase 2 – Modeling Standards
Documentation: `docs/02_modeling_standards.md`

## Phase 3 – Prepare and Explore
Documentation: `docs/03_prepare_and_explore.md`

## Phase 4 – Build Dimensions
Documentation: `docs/04_dimensions.md`

## Phase 5 – Build Fact Tables
Documentation: `docs/05_fact_sales.md`

## Phase 6 – Continue Refactoring
Documentation: `docs/06_continuing_refactoring.md`

## Phase 7 – Final Semantic Model
Documentation: `docs/07_final_model.md`

## Phase 8 – Lessons Learned
Documentation: `docs/08_lessons_learned.md`

---

# Final Semantic Model

![Final Semantic Model](images/final_semantic_model.png)

## Shared Dimensions

- dim_customer
- dim_products
- dim_geo
- dim_campaign
- dim_order_flag
- dim_date

## Fact Tables

- fact_sales
- fact_inventory
- fact_campaign
- fact_order_process
- fact_sales_target
- fact_promotion_coverage

---

# Technologies Used

| Category | Technology |
|-----------|------------|
| BI Platform | Power BI Desktop |
| Data Transformation | Power Query (M) |
| Data Modeling | Star Schema, Galaxy Schema |
| Calculations | DAX |
| Security | Dynamic Row-Level Security |
| Version Control | Git & GitHub |

---

# Repository Structure

```text
powerbi-data-model-refactoring/
├── README.md
├── docs/
├── images/
└── pbix/
```

---

# Skills Demonstrated

- Power BI
- Power Query
- DAX
- Dimensional Modeling
- Galaxy Schema
- Dynamic RLS
- Git & GitHub

---

# Power BI Files

| File | Description |
|------|-------------|
| Original Semantic Model.pbix | Original semantic model before refactoring |
| Power BI Semantic Model Refactoring.pbix | Final refactored semantic model |

---

# Project Outcome

The project transformed a legacy semantic model into a scalable Galaxy Schema with reusable dimensions, multiple fact tables, centralized DAX measures, and Dynamic Row-Level Security.

---

# Acknowledgements

The business scenario was inspired by a Power BI data modeling portfolio exercise by **Baraa**. The implementation, documentation, refactoring decisions, and repository organization were completed independently by me.
