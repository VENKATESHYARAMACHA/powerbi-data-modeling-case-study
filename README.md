# Power BI Semantic Model Refactoring

## Overview

This project demonstrates the end-to-end refactoring of a complex Power BI semantic model into a clean, scalable, and maintainable dimensional model.

Starting from an unstructured model containing duplicated tables, inconsistent naming, and unnecessary relationships, I redesigned the semantic model by applying dimensional modeling best practices. The final solution follows a Galaxy Schema (Fact Constellation), where multiple fact tables share common conformed dimensions to support different business processes.

---

## Objectives

- Refactor an existing semantic model
- Apply dimensional modeling best practices
- Create reusable dimension tables
- Build multiple fact tables
- Implement a shared date dimension
- Create reusable DAX measures
- Implement dynamic Row-Level Security (RLS)
- Produce a clean and maintainable Power BI semantic model

---

## Final Architecture

![Final Semantic Model](images/final_semantic_model.png)

---

## Features

- Galaxy Schema (Fact Constellation)
- Conformed Dimensions
- Shared Date Dimension
- Calendar and Fiscal Date Attributes
- Reusable Measures Table
- Dynamic Row-Level Security
- Clean Naming Standards
- Organized Power Query Structure

---

## Project Documentation

| Step | Document |
|------|----------|
| 1 | 01_existing_model.md |
| 2 | 02_modeling_standards.md |
| 3 | 03_prepare_and_explore.md |
| 4 | 04_dimensions.md |
| 5 | 05_fact_sales.md |
| 6 | 06_continuing_refactoring.md |
| 7 | 07_final_model.md |
| 8 | 08_lessons_learned.md |

---

## Power BI Files

| File | Description |
|------|-------------|
| **Original Semantic Model.pbix** | Original semantic model before refactoring |
| **Power BI Semantic Model Refactoring.pbix** | Final semantic model after refactoring |

---

## Skills Demonstrated

- Power Query
- Data Modeling
- Star Schema Design
- Galaxy Schema Design
- Dimensional Modeling
- DAX
- Date Dimension Design
- Dynamic Row-Level Security
- Power BI Best Practices

---

## Project Outcome

The final semantic model is organized into reusable dimensions and multiple fact tables, providing a scalable foundation for reporting and analytics. Dynamic Row-Level Security was implemented to restrict data access based on the logged-in user's assigned region, demonstrating both secure and maintainable report design.
