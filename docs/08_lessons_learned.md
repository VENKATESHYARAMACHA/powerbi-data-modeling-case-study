# Lessons Learned

Throughout this project, I gained practical experience in designing and refactoring enterprise-scale semantic models using dimensional modeling principles.

## Key Takeaways

### Understand the business before modeling

Before making structural changes, I explored every table to understand the business processes, data sources, and relationships.

Understanding the business context made it easier to identify facts, dimensions, and the appropriate grain for each table.

---

### Define the grain first

One of the most important lessons was defining the grain of every table before creating relationships.

Knowing what each row represented helped avoid incorrect joins and prevented data duplication.

---

### Build dimensions before facts

Creating reusable dimensions first simplified the development of the fact tables and reduced duplicated attributes across the model.

---

### Remove unnecessary data

Not every source table belongs in the semantic model.

Removing duplicate, unused, and disconnected tables improved both model performance and maintainability.

---

### Reuse shared dimensions

Using shared dimensions such as Customer, Product, Geography, Campaign, and Date enabled multiple business processes to be analysed consistently.

---

### Keep business processes separate

Rather than combining different business processes into one large fact table, each process was modelled independently.

Examples include:

- Sales
- Inventory
- Campaign Performance
- Promotion Coverage
- Order Process
- Sales Targets

This approach improves scalability and simplifies future development.

---

### Standardize the model

Applying consistent naming conventions, key naming, prefixes, and formatting made the semantic model easier to understand and maintain.

---

### Create reusable measures

Building reusable DAX measures provides consistent business calculations and reduces duplication across reports.

---

### Design for scalability

Using a Galaxy Schema allows additional fact tables and dimensions to be added with minimal changes to the existing model.

---

## Final Thoughts

This project provided hands-on experience with dimensional modeling, semantic model refactoring, Power Query transformations, relationship design, DAX measures, and Power BI best practices.

It also reinforced the importance of designing semantic models that are clean, scalable, and easy for report developers to use.
