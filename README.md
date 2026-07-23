# Power BI Semantic Model Refactoring: From Legacy Model to Galaxy Schema

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Modeling-F2C811?logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Galaxy%20Schema-success)
![RLS](https://img.shields.io/badge/Security-Dynamic%20RLS-orange)

> An end-to-end Power BI semantic model refactoring project demonstrating dimensional modeling, semantic model optimization, reusable DAX measures, and Dynamic Row-Level Security (RLS).

---

# Final Semantic Model

> Replace with your final semantic model screenshot.

```markdown
![Final Semantic Model](images/final_semantic_model.png)
```

---

# Project Overview

This project demonstrates the end-to-end refactoring of an existing Power BI semantic model into a clean, scalable, and enterprise-ready semantic model.

The original model contained duplicated tables, inconsistent naming conventions, unnecessary columns, and complex relationships. Instead of rebuilding the model from scratch, I analyzed the existing implementation and incrementally transformed it by applying dimensional modeling best practices.

The final solution follows a **Galaxy Schema (Fact Constellation)** with shared conformed dimensions supporting multiple business processes.

---

# Project Requirements

- Analyze the existing semantic model.
- Identify business entities and business processes.
- Apply dimensional modeling best practices.
- Create reusable conformed dimensions.
- Separate business processes into dedicated fact tables.
- Build a shared Date dimension.
- Create reusable DAX measures.
- Implement Dynamic Row-Level Security.
- Improve scalability and maintainability.

---

# Data Architecture

```text
Existing Semantic Model
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
Galaxy Schema (Fact Constellation)
```

---

# Semantic Model Refactoring

## Original Challenges

- Duplicate tables
- Inconsistent naming
- Unnecessary columns
- Complex relationships
- Difficult maintenance

## Improvements

- Created reusable dimensions
- Separated business processes into fact tables
- Optimized relationships
- Added shared Date dimension
- Centralized DAX measures
- Implemented Dynamic RLS

---

# Project Documentation

| Phase | Description |
|-------|-------------|
| 01 | Existing Model Analysis |
| 02 | Modeling Standards |
| 03 | Prepare & Explore |
| 04 | Build Dimensions |
| 05 | Build Fact Tables |
| 06 | Continue Refactoring |
| 07 | Final Semantic Model |
| 08 | Lessons Learned |

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
└── pbix/
    ├── Original Semantic Model.pbix
    └── Power BI Semantic Model Refactoring.pbix
```

---

# Technologies Used

| Category | Technology |
|----------|------------|
| BI Platform | Power BI Desktop |
| Data Transformation | Power Query (M) |
| Data Modeling | Star Schema, Galaxy Schema |
| Language | DAX |
| Security | Dynamic Row-Level Security |
| Version Control | Git & GitHub |

---

# Project Highlights

- Galaxy Schema (Fact Constellation)
- 6 Dimension Tables
- 6 Fact Tables
- Shared Date Dimension
- Dynamic Row-Level Security
- Reusable DAX Measures
- Complete end-to-end documentation

---

# Future Improvements

- Incremental Refresh
- Calculation Groups
- Deployment Pipelines
- CI/CD for Power BI
- Fabric Migration

---

# About Me

**Venkatesh Yaramacha**

Passionate about Data Analytics, Power BI, Business Intelligence, and Azure Data Engineering.

- GitHub: *(Add your profile link)*
- LinkedIn: *(Add your profile link)*

---

# Acknowledgements

The business scenario used in this project was inspired by a Power BI data modeling portfolio exercise created by **Baraa**. The semantic model implementation, refactoring decisions, documentation, and repository organization were completed independently by me as part of my learning journey and portfolio development.
