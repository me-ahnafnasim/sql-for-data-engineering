
# 📘 **DBMS Fancy Terms — Cheat Sheet with Explanation**

---
In a relational table, the first row portion that contains the **column names** is called the **header**.

### More precisely:
- ✅ **Header** — the top part of a table that lists the **attribute names** (i.e., column names).  
- Each column name in the header corresponds to an **attribute** (or field) in the relation schema.

### Example:
| **id** | **name** | **dept** | ← 🔹 **Header** (contains attribute names)  
|--------|----------|----------|  
| 101    | Alice    | CS       | ← Tuple (row)  
| 102    | Bob      | Math     | ← Tuple (row)  

---

### Related Terminology:
| Term        | Meaning |
|-------------|---------|
| **Header**  | Set of **attribute names** (column labels) — defines the *schema* of the relation. |
| **Body**    | Set of **tuples** (rows/data entries). |
| **Schema**  | Structure: `RelationName(attribute₁, attribute₂, …)` — defined by the header + domains. |
| **Relation** | = **Header** + **Body** (i.e., the full table). |

> 📌 Note: In formal relational theory (Codd’s model), a relation is an *unordered* set of tuples — so technically, tables don’t have a “first row” for data, but the **header** is still a distinct structural component.


# 🔵 **1. Relational Model Terms**


### ⚠️ Terminology Note:
- In **relational database theory**, the word **“relation”** is synonymous with **table** (a set of tuples/rows).
- But in **ER modeling**, we say **“relationship”** — not “relation” — to avoid confusion.
  - So:  
    - ER Model → *Entity* and *Relationship*  
    - Relational Model → *Relation* = Table

---





### **Relation**

A table that stores data as rows and columns.

### **Tuple**

A single **row** in a relation.

### **Attribute**

A **column** in a table.

### **Degree**

Number of attributes (columns) in a relation.

### **Cardinality**

Number of tuples (rows) in a relation.

### **Domain**

Set of valid values for an attribute
(e.g., age domain = integers 0–120).

### **Schema**

Blueprint/structure of a table
(id INT, name VARCHAR).

### **Instance**

Actual data stored at any moment.

### **Super Key**

Any set of attributes that uniquely identifies a row.

### **Candidate Key**

Minimal super key → no attribute can be removed.

### **Primary Key**

Chosen candidate key for identification.

### **Alternate Key**

Other candidate keys not chosen as primary.

### **Composite Key**

A key made of **multiple attributes**.

### **Surrogate Key**

Artificial key created by the system (e.g., auto-increment ID).

### **Foreign Key**

Attribute that creates a link between two tables.

### **Referential Integrity**

Ensures foreign key values always reference valid records.

---

# 🟣 **2. ER Model Terms (Entity-Relationship)**

### **Entity**

A real-world object (Customer, Product).

### **Entity Set**

Collection of similar entities.

### **Weak Entity**

Depends on another entity; cannot exist alone.

### **Partial Key**

The attribute that uniquely identifies a weak entity.

### **Participation**

Whether an entity must participate in a relation.
**Total** (must participate) / **Partial** (optional).

### **Mapping Cardinality**

Type of relationship:
1:1, 1:N, M:N.

---

# 🟡 **3. Normalization Terms**

### **Functional Dependency (FD)**

Relationship where one attribute determines another.
A → B means A determines B.

### **Determinant**

Left side of an FD (A in A → B).

### **Partial Dependency**

Non-key attribute depends on **part of a composite key** (2NF issue).

### **Transitive Dependency**

A → B and B → C
(C indirectly depends on A).

### **Anomalies**

Problems in unnormalized tables:
Insertion, Update, Deletion issues.

### **Normal Forms**

* **1NF** – No repeating groups; atomic values.
* **2NF** – No partial dependency.
* **3NF** – No transitive dependency.
* **BCNF** – Every determinant is a candidate key.
* **4NF/5NF** – Deals with multi-valued and join dependencies.

### **Lossless Decomposition**

Splitting tables without losing data.

### **Dependency Preservation**

FDs must still be enforceable after decomposition.

---

# 🔴 **4. Relational Algebra Terms**

### **Selection (σ)**

Filters rows based on a condition.

### **Projection (π)**

Selects specific columns.

### **Cartesian Product (×)**

Combines all rows of two relations.

### **Union (∪)**

Combines rows from two relations (no duplicates).

### **Intersection (∩)**

Rows common to both relations.

### **Difference (−)**

Rows in A but not in B.

### **Join (⨝)**

Combines rows based on matching attributes.

Types: natural, equi, theta, outer join.

### **Division (÷)**

Useful for "for all" queries.

### **Renaming (ρ)**

Changes relation or attribute names.

---

# 🟢 **5. SQL Terms**

### **DDL**

Define structure (CREATE, ALTER, DROP).

### **DML**

Manipulate data (INSERT, UPDATE, DELETE).

### **DCL**

Access control (GRANT, REVOKE).

### **TCL**

Transaction control (COMMIT, ROLLBACK).

### **View**

Virtual table defined by a query.

### **Materialized View**

Stored physical copy of a query result.

### **Stored Procedure**

Precompiled SQL code saved in DB.

### **Trigger**

Automatic action fired by insert/update/delete.

### **Cursor**

Row-by-row data processing mechanism.

### **Scalar Function**

Returns a single value (e.g., CONCAT).

### **Aggregate Function**

Works on groups (SUM, MAX).

### **Window Function**

Calculates values over a row window.

### **Subquery**

Query inside another query.

### **Correlated Subquery**

Subquery that depends on outer query.

---

# 🟤 **6. Indexing Terms**

### **B+ Tree Index**

Tree-based index for range queries.

### **Hash Index**

Fast exact-match lookup (key = value).

### **Clustered Index**

Physically sorts table based on index.

### **Non-Clustered Index**

Separate index structure pointing to data.

### **Dense Index**

Every record has an index entry.

### **Sparse Index**

Only some records have entries.

### **Primary/Secondary Index**

Based on primary key vs non-primary attributes.

---

# 🟠 **7. Storage & File Structure**

### **Page/Block**

Smallest unit of disk I/O.

### **Slotted Page**

Structure that manages variable-length records.

### **Heap File**

Records stored in no particular order.

### **Sequential File**

Records stored sorted by a key.

### **Buffer Manager**

Manages memory–disk transfer.

### **Page Replacement Policies**

E.g., LRU, FIFO.

---

# 🟤 **8. Transactions & Concurrency**

### **ACID**

Guarantees correct transactions.

### **Schedule**

Order in which transactions execute.

### **Serializable**

Equivalent to some serial schedule; ensures correctness.

### **Conflict Serializability**

Checks if swapping non-conflicting operations gives a serial order.

### **Locks**

Used to control concurrency (read/write).

### **2PL (Two-Phase Locking)**

Protocol ensuring serializability.

### **Deadlock**

Two transactions wait forever for each other.

### **WAL (Write-Ahead Logging)**

Log changes before applying them to DB.

### **Checkpoint**

Savepoint for faster recovery.

---

# 🔵 **9. Distributed DB Terms**

### **Sharding**

Splitting data horizontally.

### **Replication**

Duplicating data across nodes.

### **Fragmentation**

Splitting data logically (horizontal/vertical).

### **CAP Theorem**

Cannot have all 3: Consistency, Availability, Partition-Tolerance.

### **2PC**

Protocol ensuring distributed commit.

### **Consistency Models**

Strong, Eventual, Causal.

### **Leader Election**

Choosing a coordinator node.

### **Consensus Protocols**

Ensures distributed agreement (Raft, Paxos).

---



