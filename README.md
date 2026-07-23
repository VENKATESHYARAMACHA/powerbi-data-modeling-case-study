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

This project demonstrates the end-to-end process of refactoring an existing Power BI semantic model into a clean, scalable, and enterprise-ready semantic model.

The original model contained duplicated tables, inconsistent naming conventions, unnecessary columns, and complex relationships that made it difficult to understand, maintain, and extend.

Instead of rebuilding the solution from scratch, I analyzed the existing implementation, identified opportunities for improvement, and incrementally transformed the model by applying dimensional modeling principles and Power BI best practices.

The final solution follows a **Galaxy Schema (Fact Constellation)**, where multiple business processes share conformed dimensions, providing a scalable and maintainable foundation for business reporting and analytics.

---

# Table of Contents

- [Key Achievements](#key-achievements)
- [Final Semantic Model](#final-semantic-model)
- [Project Objectives](#project-objectives)
- [Development Process](#development-process)
- [Technologies Used](#technologies-used)
- [Final Architecture](#final-architecture)
- [Repository Structure](#repository-structure)
- [Skills Demonstrated](#skills-demonstrated)
- [Power BI Files](#power-bi-files)
- [Project Outcome](#project-outcome)
- [Acknowledgements](#acknowledgements)

---

# Key Achievements

- Refactored a legacy semantic model into a **Galaxy Schema (Fact Constellation)**.
- Designed **6 conformed dimension tables**.
- Built **6 fact tables** supporting multiple business processes.
- Created a shared **Date Dimension** with calendar and fiscal attributes.
- Developed centralized and reusable **DAX measures**.
- Implemented **Dynamic Row-Level Security (RLS)**.
- Organized Power Query using a structured folder hierarchy.
- Documented the complete end-to-end semantic model refactoring process.

---

# Final Semantic Model

The completed semantic model follows a **Galaxy Schema (Fact Constellation)** consisting of multiple fact tables connected through shared conformed dimensions.

![Final Semantic Model](images/final_semantic_model.png)

---

# Project Objectives

The primary objectives of this project were to:

- Analyze the existing semantic model.
- Understand the business processes.
- Apply dimensional modeling best practices.
- Create reusable dimension tables.
- Separate business processes into dedicated fact tables.
- Build a shared Date dimension.
- Develop reusable DAX measures.
- Implement Dynamic Row-Level Security (RLS).
- Improve scalability, maintainability, and readability.

---

# Development Process

The semantic model was developed incrementally through the following phases.

---

## Phase 1 – Understanding the Existing Model

Before making any changes, I explored the existing semantic model to understand the business requirements, identify business entities, and evaluate the current design.

**Activities**

- Explored every table in the semantic model.
- Identified business entities and transactional data.
- Reviewed existing relationships.
- Documented modeling issues and improvement opportunities.

📖 **Read more:**  
➡️ **[01 – Existing Model Analysis](docs/01_existing_model.md)**

---

## Phase 2 – Defining Modeling Standards

After understanding the existing model, I established consistent modeling standards to guide the refactoring process.

**Activities**

- Table naming conventions
- Column naming conventions
- Primary and foreign key standards
- Query organization
- Relationship design principles
- Dimensional modeling guidelines

📖 **Read more:**  
➡️ **[02 – Modeling Standards](docs/02_modeling_standards.md)**

---

## Phase 3 – Preparing and Exploring the Model

The semantic model was prepared by reviewing every query, organizing Power Query, and planning the target architecture.

**Activities**

- Organized Power Query into logical folders.
- Reviewed every query.
- Removed unnecessary objects.
- Planned the target semantic model.

📖 **Read more:**  
➡️ **[03 – Prepare and Explore](docs/03_prepare_and_explore.md)**

---

## Phase 4 – Building Dimension Tables

Reusable dimension tables were created to support multiple business processes.

**Dimensions Created**

- dim_customer
- dim_products
- dim_geo
- dim_campaign
- dim_order_flag
- dim_date

📖 **Read more:**  
➡️ **[04 – Building Dimensions](docs/04_dimensions.md)**

---

## Phase 5 – Building Fact Tables

Business processes were separated into dedicated fact tables to improve scalability and simplify reporting.

**Fact Tables Created**

- fact_sales
- fact_inventory
- fact_campaign
- fact_order_process
- fact_sales_target
- fact_promotion_coverage

📖 **Read more:**  
➡️ **[05 – Building Fact Tables](docs/05_fact_sales.md)**

---

## Phase 6 – Continuing the Refactoring

The semantic model was further refined by improving relationships, optimizing queries, and enhancing the overall model.

**Activities**

- Relationship refinement
- Query optimization
- Additional fact tables
- Model improvements
- Semantic model optimization

📖 **Read more:**  
➡️ **[06 – Continuing Refactoring](docs/06_continuing_refactoring.md)**

---

## Phase 7 – Finalizing the Semantic Model

The final stage focused on completing and validating the semantic model.

**Activities**

- Built a shared Date dimension
- Added calendar and fiscal attributes
- Created reusable DAX measures
- Implemented Dynamic Row-Level Security
- Validated relationships
- Tested security implementation
- Reviewed modeling standards

📖 **Read more:**  
➡️ **[07 – Final Semantic Model](docs/07_final_model.md)**

---

## Phase 8 – Lessons Learned

The project concludes with lessons learned and best practices that will guide future semantic modeling projects.

**Topics Covered**

- Dimensional modeling
- Fact and dimension design
- Reusable semantic models
- Scalability
- Performance considerations
- Project reflections

📖 **Read more:**  
➡️ **[08 – Lessons Learned](docs/08_lessons_learned.md)**

---

# Technologies Used

| Category | Technology |
|-----------|------------|
| BI Platform | Power BI Desktop |
| Data Transformation | Power Query (M) |
| Data Modeling | Star Schema, Galaxy Schema |
| Calculations | DAX |
| Security | Dynamic Row-Level Security |
| Documentation | Markdown |
| Version Control | Git & GitHub |

---

# Final Architecture

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

# Repository Structure

```text
powerbi-data-model-refactoring/
│
├── README.md
├── docs/
│   ├── 01_existing_model.md
│   ├── 02_modeling_standards.md
│   ├── 03_prepare_and_explore.md
│   ├── 04_dimensions.md
│   ├── 05_fact_sales.md
│   ├── 06_continuing_refactoring.md
│   ├── 07_final_model.md
│   └── 08_lessons_learned.md
│
├── images/
│
└── pbix/
    ├── Original Semantic Model.pbix
    └── Power BI Semantic Model Refactoring.pbix
```

---

# Skills Demonstrated

- Power BI
- Power Query
- Data Modeling
- Dimensional Modeling
- Galaxy Schema Design
- Star Schema Design
- DAX
- Date Dimension Design
- Dynamic Row-Level Security
- Semantic Model Optimization
- Git & GitHub Documentation

---

# Power BI Files

| File | Description |
|------|-------------|
| **Original Semantic Model.pbix** | Original semantic model before refactoring |
| **Power BI Semantic Model Refactoring.pbix** | Final refactored semantic model |

---

# Project Outcome

This project transformed an unstructured semantic model into a clean, scalable, and maintainable **Galaxy Schema (Fact Constellation)** by applying dimensional modeling best practices.

The final semantic model includes reusable dimensions, multiple fact tables, a shared Date dimension, centralized DAX measures, and Dynamic Row-Level Security, resulting in a solution that is easier to understand, maintain, extend, and use for business reporting and analytics.

---

# Acknowledgements

This project was developed as part of my learning journey in Power BI semantic modeling and dimensional modeling.

The business scenario was inspired by a Power BI data modeling portfolio exercise created by **Baraa**. The semantic model implementation, refactoring decisions, documentation, GitHub repository structure, screenshots, and project presentation included in this repository were completed independently to demonstrate my understanding and practical application of Power BI data modeling best practices.
