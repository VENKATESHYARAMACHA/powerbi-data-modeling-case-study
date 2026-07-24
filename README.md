# Power BI Semantic Model Refactoring: From Legacy Model to Galaxy Schema

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Modeling-F2C811?logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Galaxy Schema](https://img.shields.io/badge/Data%20Model-Galaxy%20Schema-success)

> Refactoring an existing Power BI semantic model into a clean, scalable, and enterprise-ready semantic model by applying dimensional modeling best practices.

---

# Project Overview

This project demonstrates the complete process of refactoring an existing Power BI semantic model. Instead of rebuilding the model from scratch, I analyzed the existing implementation, identified design issues, and incrementally transformed the model using dimensional modeling best practices.

The complete refactoring journey is documented step by step in this repository.

---

# The Challenge

The original semantic model had several design challenges:

- Duplicate descriptive data
- Complex relationships
- Inconsistent naming conventions
- Unnecessary columns
- Mixed business processes
- Difficult maintenance
- Limited scalability

These issues made the semantic model difficult to understand, maintain, and extend.

---

# Original Semantic Model

The image below shows the original semantic model before refactoring.

![Original Semantic Model](images/original_semantic_model.png)

The goal of this project was to improve the semantic model while preserving the existing business logic.

---

# Refactoring Strategy

Rather than making all the changes at once, I improved the semantic model incrementally. Each phase focused on one area of the model, making it easier to validate changes and document the design decisions.

---

# Development Process

The semantic model was developed incrementally through the following phases.

---

## Phase 1 – Understanding the Existing Model

Before making any changes, I explored the existing semantic model to understand the business requirements, identify business entities, and evaluate the current design.

### What I did

- Explored every table in the semantic model.
- Identified business entities and transactional data.
- Reviewed existing relationships.
- Documented modeling issues and improvement opportunities.

📖 **Detailed documentation:**  
➡️ **[01 – Existing Model Analysis](docs/01_existing_model.md)**

---

## Phase 2 – Defining Modeling Standards

After understanding the existing model, I established consistent modeling standards to guide the refactoring process.

### What I did

- Defined table naming conventions.
- Standardized column naming.
- Planned relationship design.
- Established dimensional modeling guidelines.

📖 **Detailed documentation:**  
➡️ **[02 – Modeling Standards](docs/02_modeling_standards.md)**

---

## Phase 3 – Preparing and Exploring the Model

The semantic model was prepared by reviewing every query, organizing Power Query, and planning the target architecture.

### What I did

- Organized Power Query into logical folders.
- Reviewed every query.
- Removed unnecessary objects.
- Planned the target semantic model.

📖 **Detailed documentation:**  
➡️ **[03 – Prepare and Explore](docs/03_prepare_and_explore.md)**

---

## Phase 4 – Building Dimension Tables

Reusable dimension tables were created to support multiple business processes.

### What I did

- Created reusable conformed dimension tables.
- Consolidated descriptive business information.
- Designed dimensions shared across multiple fact tables.

**Dimensions**

- dim_customer
- dim_products
- dim_geo
- dim_campaign
- dim_order_flag
- dim_date

📖 **Detailed documentation:**  
➡️ **[04 – Building Dimensions](docs/04_dimensions.md)**

---

## Phase 5 – Building Fact Tables

Business processes were separated into dedicated fact tables to improve scalability and simplify reporting.

### What I did

- Identified individual business processes.
- Created dedicated fact tables.
- Established a consistent grain for reporting.

**Fact Tables**

- fact_sales
- fact_inventory
- fact_campaign
- fact_order_process
- fact_sales_target
- fact_promotion_coverage

📖 **Detailed documentation:**  
➡️ **[05 – Building Fact Tables](docs/05_fact_sales.md)**

---

## Phase 6 – Continuing the Refactoring

The semantic model was further refined by improving relationships, optimizing queries, and enhancing the overall model.

### What I did

- Refined relationships.
- Optimized Power Query.
- Improved semantic model structure.
- Enhanced maintainability.

📖 **Detailed documentation:**  
➡️ **[06 – Continuing Refactoring](docs/06_continuing_refactoring.md)**

---

## Phase 7 – Finalizing the Semantic Model

The final stage focused on completing and validating the semantic model.

### What I did

- Built a shared Date dimension.
- Created reusable DAX measures.
- Implemented Dynamic Row-Level Security.
- Validated the final semantic model.

📖 **Detailed documentation:**  
➡️ **[07 – Final Semantic Model](docs/07_final_model.md)**

---

## Phase 8 – Lessons Learned

The project concludes with lessons learned and best practices that will guide future semantic modeling projects.

### Topics Covered

- Dimensional modeling
- Fact and dimension design
- Reusable semantic models
- Scalability
- Performance considerations
- Project reflections

📖 **Detailed documentation:**  
➡️ **[08 – Lessons Learned](docs/08_lessons_learned.md)**

---

# Final Semantic Model

The completed semantic model follows a **Galaxy Schema (Fact Constellation)**.

![Final Semantic Model](images/final_semantic_model.png)

---

# What I Learned

Through this project I gained practical experience in:

- Semantic model refactoring
- Dimensional modeling
- Star Schema and Galaxy Schema design
- Power Query organization
- DAX best practices
- Dynamic Row-Level Security
- Designing scalable Power BI semantic models

---

# Conclusion

This project demonstrates how an existing semantic model can be transformed into a clean, scalable, and maintainable solution by applying dimensional modeling best practices. The detailed documentation in this repository captures every stage of the refactoring journey.

---

# Acknowledgements

The business scenario used in this project was inspired by a Power BI data modeling portfolio exercise by **Baraa**. The implementation, refactoring decisions, documentation, and repository organization were completed independently as part of my learning journey.
