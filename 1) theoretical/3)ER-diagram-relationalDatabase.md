# ✅ Updated ER Diagram vs Relational Model Terms (FULL Table)

| **ER Diagram (ER Model / Conceptual Terms)** | **Relational Model (Relational Schema / Table Terms)** |
| -------------------------------------------- | ------------------------------------------------------ |
| **Entity**                                   | **Table / Relation**                                   |
| **Entity Set**                               | **Relation (Table)**                                   |
| **Entity Instance**                          | **Tuple (Row)**                                        |
| **Attribute**                                | **Attribute / Column (Field)**                         |
| **Key Attribute**                            | **Primary Key Attribute**                              |
| **Composite Attribute**                      | **Multiple Columns**                                   |
| **Multivalued Attribute**                    | **Separate Relation (New Table)**                      |
| **Derived Attribute**                        | **Computed / Derived Column (not stored)**             |
| **Domain (implicit)**                        | **Domain (explicit: datatype + constraints)**          |
| **Relationship**                             | **Foreign Key / Link between relations**               |
| **Relationship Set**                         | **Foreign Key Constraint / Associative Table**         |
| **1:1, 1:N, M:N (Mapping Cardinality)**      | **Key Constraints + Foreign Keys**                     |
| **M:N Relationship**                         | **New Relation (Bridge / Junction Table)**             |
| **Participation (Total/Partial)**            | **NOT NULL / Optional FK constraint**                  |
| **Weak Entity**                              | **Table with Composite Primary Key**                   |
| **Partial Key (Weak Entity discriminator)**  | **Part of Composite Primary Key**                      |
| **Identifying Relationship**                 | **Foreign key included in Primary Key**                |
| **Generalization / Specialization (ISA)**    | **Table inheritance / multiple table mapping**         |
| **ER Diagram (Conceptual Schema)**           | **Relational Schema (Tables + constraints)**           |
| **Key (in ER: identifiers)**                 | **Primary Key / Candidate Key**                        |
| **Composite Key (ER)**                       | **Composite Primary Key**                              |
| **---**                                      | **Super Key**                                          |
| **---**                                      | **Candidate Key**                                      |
| **---**                                      | **Alternate Key**                                      |
| **---**                                      | **Surrogate Key**                                      |
| **---**                                      | **Referential Integrity**                              |
| **---**                                      | **Degree (no. of columns)**                            |
| **---**                                      | **Cardinality (no. of rows)**                          |
| **---**                                      | **Schema (table structure definition)**                |
| **---**                                      | **Instance (current table data)**                      |

---

## ✅ Notes (Important for Exam)

* In ER model, **keys exist**, but terms like **super key / candidate key / alternate key** are mostly used in the **relational model**.
* **Degree & Cardinality** are formal relational terms:

  * Degree → columns
  * Cardinality → rows

---