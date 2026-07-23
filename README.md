# Power BI Semantic Model Refactoring: From Legacy Model to Galaxy Schema

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Modeling-F2C811?logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Galaxy%20Schema-success)
![RLS](https://img.shields.io/badge/Security-Dynamic%20RLS-orange)

> End-to-end Power BI Semantic Model Refactoring demonstrating dimensional modeling, semantic model optimization, reusable DAX measures, and Dynamic Row-Level Security.

---

# Project Overview

This project documents my journey of transforming an existing Power BI semantic model into a clean, scalable and enterprise-ready semantic model.

Instead of rebuilding the model from scratch, I first analyzed the existing implementation, understood the business processes, identified modeling issues, and then incrementally refactored the model using dimensional modeling best practices.

The final solution follows a **Galaxy Schema (Fact Constellation)**.

---

# Business Problem

The original semantic model had several design challenges:

- Duplicate descriptive data
- Inconsistent naming conventions
- Unnecessary columns
- Complex relationships
- Mixed business processes
- Difficult maintenance
- Limited scalability

These issues reduced readability, increased maintenance effort, and made future enhancements more difficult.

---

# Project Objectives

- Understand the existing semantic model
- Identify business entities and business processes
- Design reusable conformed dimensions
- Separate business processes into dedicated fact tables
- Build a shared Date dimension
- Create reusable DAX measures
- Implement Dynamic Row-Level Security
- Improve scalability and maintainability

---

# Solution Overview

Rather than redesigning everything from scratch, I adopted an incremental refactoring approach.

The project included:

- Exploring the existing semantic model
- Defining modeling standards
- Creating reusable dimension tables
- Designing dedicated fact tables
- Simplifying relationships
- Building a shared Date dimension
- Centralizing DAX measures
- Implementing Dynamic RLS
- Validating the final semantic model

---

# Original Semantic Model

> Add screenshot

```markdown
![Original Model](images/original_model.png)
```

Key issues identified:

- Duplicate tables
- Redundant attributes
- Complex relationships
- Inconsistent model design

---

# Refactoring Journey

```text
Existing Model
      │
      ▼
Business Understanding
      │
      ▼
Dimension Design
      │
      ▼
Fact Table Design
      │
      ▼
Relationship Optimization
      │
      ▼
Shared Date Dimension
      │
      ▼
Reusable DAX Measures
      │
      ▼
Dynamic Row-Level Security
      │
      ▼
Final Galaxy Schema
```

---

# Final Semantic Model

```markdown
![Final Semantic Model](images/final_semantic_model.png)
```

Shared Dimensions

- dim_customer
- dim_products
- dim_geo
- dim_campaign
- dim_order_flag
- dim_date

Fact Tables

- fact_sales
- fact_inventory
- fact_campaign
- fact_order_process
- fact_sales_target
- fact_promotion_coverage

---

# Project Documentation

| Phase | Documentation |
|------|----------------|
|01|Existing Model Analysis|
|02|Modeling Standards|
|03|Prepare and Explore|
|04|Building Dimensions|
|05|Building Fact Tables|
|06|Continuing Refactoring|
|07|Final Semantic Model|
|08|Lessons Learned|

Documentation files are available in the **docs/** folder.

---

# Repository Structure

```text
powerbi-data-model-refactoring/
│
├── README.md
├── docs/
├── images/
└── pbix/
```

---

# Technologies Used

| Category | Technology |
|-----------|------------|
| BI | Power BI Desktop |
| ETL | Power Query (M) |
| Modeling | Star Schema, Galaxy Schema |
| Calculations | DAX |
| Security | Dynamic Row-Level Security |
| Version Control | Git & GitHub |

---

# Project Results

The refactored semantic model delivers:

- Cleaner and more maintainable model
- Reusable conformed dimensions
- Dedicated fact tables
- Shared Date dimension
- Simplified relationships
- Dynamic Row-Level Security
- Improved scalability
- Better foundation for analytical reporting

---

# Future Improvements

- Incremental Refresh
- Calculation Groups
- Microsoft Fabric Migration
- Deployment Pipelines
- Automated Testing

---

# Acknowledgements

The business scenario used in this project was inspired by a Power BI data modeling portfolio exercise by **Baraa**. The implementation, refactoring decisions, documentation, and repository organization were completed independently by me as part of my learning journey.
