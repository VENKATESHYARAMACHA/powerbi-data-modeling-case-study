# Power BI Semantic Model Refactoring

> Refactoring a complex Power BI semantic model into a clean, scalable, and maintainable Galaxy Schema (Fact Constellation) by applying dimensional modeling best practices.

![Final Semantic Model](images/final_semantic_model.png)

---

# Overview

This project demonstrates the complete process of refactoring an existing Power BI semantic model into a well-structured, enterprise-ready semantic model.

The original model contained duplicated tables, inconsistent naming conventions, unnecessary columns, and relationships that made the model difficult to maintain and scale.

Instead of rebuilding the model from scratch, I analyzed the existing implementation, identified improvement opportunities, and incrementally transformed it by applying dimensional modeling principles and Power BI best practices.

The final solution follows a **Galaxy Schema (Fact Constellation)**, where multiple business processes share common conformed dimensions to provide a scalable and maintainable foundation for reporting and analytics.

---

# Project Objectives

- Analyze the existing semantic model
- Understand the business processes
- Apply dimensional modeling best practices
- Create reusable dimension tables
- Separate business processes into individual fact tables
- Build a shared Date dimension
- Develop reusable DAX measures
- Implement Dynamic Row-Level Security (RLS)
- Improve scalability and maintainability

---

# Development Process

The semantic model was developed incrementally through the following phases. Each phase is documented in detail to demonstrate the complete refactoring process.

---

## Phase 1 – Understanding the Existing Model

Before making any changes, I explored the existing semantic model to understand the business, identify key entities, and evaluate the current design.

Activities included:

- Explored every table in the semantic model.
- Identified business entities and transactional data.
- Reviewed existing relationships.
- Documented modeling issues and improvement opportunities.

📖 **Detailed documentation:**  
➡️ [01 - Existing Model Analysis](docs/01_existing_model.md)

---

## Phase 2 – Defining Modeling Standards

After understanding the model, I established modeling standards to ensure consistency throughout the refactoring process.

Activities included:

- Table naming standards
- Column naming standards
- Primary and foreign key conventions
- Query organization
- Dimensional modeling guidelines
- Relationship design standards

📖 **Detailed documentation:**  
➡️ [02 - Modeling Standards](docs/02_modeling_standards.md)

---

## Phase 3 – Preparing and Exploring the Model

The next step was preparing the semantic model by reviewing every query and organizing Power Query into logical groups.

Activities included:

- Organized Power Query into logical folders.
- Reviewed every query individually.
- Removed unnecessary objects.
- Planned the target semantic model.

📖 **Detailed documentation:**  
➡️ [03 - Prepare and Explore](docs/03_prepare_and_explore.md)

---

## Phase 4 – Building Dimension Tables

Dimension tables were created to store descriptive business information that could be reused across multiple business processes.

Created dimensions:

- Customer
- Product
- Geography
- Campaign
- Order Flag
- Date

📖 **Detailed documentation:**  
➡️ [04 - Building Dimensions](docs/04_dimensions.md)

---

## Phase 5 – Building Fact Tables

Business processes were separated into dedicated fact tables to improve scalability and maintainability.

Fact tables created:

- Fact Sales
- Fact Inventory
- Fact Campaign
- Fact Order Process
- Fact Sales Target
- Fact Promotion Coverage (Factless Fact)

📖 **Detailed documentation:**  
➡️ [05 - Building Fact Tables](docs/05_fact_sales.md)

---

## Phase 6 – Continuing the Refactoring

The semantic model was further enhanced by refining relationships, improving model organization, and expanding the dimensional model.

Activities included:

- Additional fact tables
- Relationship refinement
- Model optimization
- Semantic model improvements

📖 **Detailed documentation:**  
➡️ [06 - Continuing Refactoring](docs/06_continuing_refactoring.md)

---

## Phase 7 – Finalizing the Semantic Model

The final stage focused on completing the semantic model by implementing reusable measures, a shared Date dimension, Dynamic Row-Level Security, and validating the completed solution.

Activities included:

- Shared Date Dimension
- Calendar & Fiscal Attributes
- Reusable DAX Measures
- Dynamic Row-Level Security
- Final Validation

📖 **Detailed documentation:**  
➡️ [07 - Final Semantic Model](docs/07_final_model.md)

---

## Phase 8 – Lessons Learned

Finally, I documented the key lessons learned throughout the project, including best practices and design decisions that will guide future semantic modeling projects.

Topics covered:

- Dimensional modeling principles
- Fact and dimension design
- Reusable semantic models
- Performance considerations
- Project reflections

📖 **Detailed documentation:**  
➡️ [08 - Lessons Learned](docs/08_lessons_learned.md)

---

# Final Architecture

The completed semantic model follows a **Galaxy Schema (Fact Constellation)** consisting of multiple fact tables connected through shared conformed dimensions.

### Shared Dimensions

- dim_customer
- dim_products
- dim_geo
- dim_campaign
- dim_order_flag
- dim_date

### Fact Tables

- fact_sales
- fact_inventory
- fact_campaign
- fact_order_process
- fact_sales_target
- fact_promotion_coverage

---

# Repository Structure

```
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

# Project Documentation

The complete development process is documented in detail.

| Step | Description |
|------|-------------|
| 01 | Existing Model Analysis |
| 02 | Modeling Standards |
| 03 | Preparing & Exploring |
| 04 | Building Dimensions |
| 05 | Building Fact Tables |
| 06 | Continuing Refactoring |
| 07 | Final Semantic Model |
| 08 | Lessons Learned |

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

---

# Power BI Files

| File | Description |
|------|-------------|
| **Original Semantic Model.pbix** | Original semantic model before refactoring |
| **Power BI Semantic Model Refactoring.pbix** | Final refactored semantic model |

---

# Project Outcome

This project transformed an unstructured semantic model into a clean, scalable, and maintainable Galaxy Schema by applying dimensional modeling best practices.

The final semantic model includes reusable dimensions, multiple fact tables, a shared Date dimension, centralized DAX measures, and dynamic Row-Level Security, providing a strong foundation for business reporting and analytics.

---

## Acknowledgements

The business scenario used in this project was inspired by a Power BI data modeling portfolio exercise by Baraa. All implementation, semantic model design, refactoring decisions, documentation, and portfolio presentation in this repository were completed independently by me.

---

# Author

**Venkatesh Yaramasa**

Data Analyst | Power BI Developer | Business Intelligence Enthusiast
