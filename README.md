
# 🗄️ SQL Learning Journey — Structured Mastery of Databases

*A structured path from DB theory (ER diagrams, normalization) to hands-on SQL Server practice. Designed for systematic mastery.*

---

## 📁 Repository Structure

```
DATABASE/
├── 1) theoretical/              # Core concepts & visual guides
│   ├── roadmap.md              # Learning sequence & milestones
│   ├── fancy-terms.md          # Glossary of essential terminology
│   ├── ER-diagram-relationalDatabase.md
│   ├── Three-Schema-Architecture.md
│   ├── type-of-relationship.md
│   ├── relationshipVSjoin.md
│   ├── Complete_DBMS_Notes.md  # Comprehensive reference (see TOC below)
│   │   ├── 1. Database Fundamentals
│   │   ├── 2. File System vs DBMS
│   │   ├── 3. Components of DBMS
│   │   ├── 4. Database Architecture
│   │   ├── 5. OLAP vs OLTP
│   │   ├── 6. Data Abstraction
│   │   ├── 7. Data Independence
│   │   ├── 8. Database Schema
│   │   ├── 9. Constraints
│   │   ├── 10. Types of Keys
│   │   ├── 11. ER Diagrams
│   │   ├── 12. Types of Attributes
│   │   ├── 12. Design Technique Model
│   │   ├── 13. Normalization
│   │   ├── 14. Relational-algebra
│   │   ├── 15. SQL Joins
│   │   ├── 16. Transactions
│   │   └── 17. DBMS Terminology Reference
│   ├── Key.md                  # Deep dive on key types
│   └── *.png / *.jpg           # Visual aids: ERD symbols, joins, normalization
├── 2) practical-sql/           # Hands-on implementation
│   └── sql-server/
│       ├── init-sqlserver-mydatabase.sql   # Sample DB setup script
│       ├── init-sqlserver-salesdb.sql      # Sales DB setup script
│       ├── *.bak               # Ready-to-restore database backups
│       └── *.pdf               # Quick-reference guides (DDL, DML, Joins, etc.)
├── 3) resources/               # Curated learning assets
│   ├── book/                   # "Database System Concepts" (textbook)
│   ├── sql-data-analytics-project/
│   ├── sql-data-warehouse-project/
│   └── sql-ultimate-course-main/
└── Theoretical Exercises/      # Chapter-wise problem sets (Chap 3 & 4)
```

---

## ⚙️ SQL Server Setup Guide (Practical Section)

### ✅ Step 1: Install SQL Server Management Studio (SSMS)

> **Note**: The latest stable version is **SSMS 19.x** (released 2023–2024). Microsoft does not use "SSMS 21" naming—this likely refers to SQL Server 2022 compatibility. SSMS 19.x fully supports SQL Server 2022.

#### Installation Steps:
1. **Download SSMS**  
   → Go to official download page: https://aka.ms/ssmsfullsetup  
   → Click **"Download SQL Server Management Studio (SSMS)"**

2. **Run Installer**  
   → Locate downloaded `SSMS-Setup-ENU.exe`  
   → Right-click → **Run as administrator**  
   → Accept license terms → Click **Install**

3. **Complete Setup**  
   → Wait for installation (~5–10 mins)  
   → Click **Close** when finished  
   → *Optional but recommended*: Restart your computer

4. **Verify Installation**  
   → Press `Win + S` → Type "SSMS" → Open **SQL Server Management Studio**  
   → Version check: `Help → About` → Should show **v19.x.x**

---

### ✅ Step 2: Connect to SQL Server

| Scenario | Server Name | Authentication | Notes |
|----------|-------------|----------------|-------|
| **Local default instance** | `localhost` or `.` | Windows Authentication | Use this if you installed SQL Server locally |
| **No local SQL Server?** | — | — | Use **Azure Data Studio** (free) or install SQL Server Express first |

> 💡 **Don't have SQL Server installed?**  
> → Download **SQL Server 2022 Express (free)**: https://www.microsoft.com/sql-server/sql-server-downloads  
> → During install: Select "Basic" → Note the **instance name** (usually `SQLEXPRESS`)  
> → Connect in SSMS using: `localhost\SQLEXPRESS`

---

### ✅ Step 3: Restore Practice Databases

```sql
-- Method 1: Using .bak files (recommended)
-- In SSMS: Right-click Databases → Restore Database → Device → Add .bak file

-- Method 2: Run initialization scripts
-- Open init-sqlserver-mydatabase.sql in SSMS → Click "Execute" (F5)
```

> 📌 **Critical Tip**: Keep `Execution order.pdf` open while practicing—it shows the *logical* query execution sequence (`FROM` → `WHERE` → `GROUP BY` → `HAVING` → `SELECT` → `ORDER BY`), which differs from written order.

---

## 🧭 Recommended Learning Path

1. **Theory First**  
   → Read `roadmap.md` → Study `Complete_DBMS_Notes.md` → Review visual aids

2. **Validate Understanding**  
   → Solve problems in `Theoretical Exercises/` *before* writing code

3. **Hands-On Practice**  
   → Install SSMS (above) → Restore `.bak` files → Experiment with PDF guides

4. **Extend Knowledge**  
   → Explore projects in `resources/` (analytics, warehousing)

---

## 📌 Quick Reference Cheat Sheet

| Concept | Files to Pair |
|---------|---------------|
| **Keys** | `Key.md` + `typesOfKeys.jpg` + `key.jpg` |
| **Joins** | `relationshipVSjoin.md` + `img-type-of-joins.png` + `Join.pdf` |
| **Normalization** | `normalization1.png` → `normalization2.png` (sequential) |
| **ER Diagrams** | `ER-diagram-relationalDatabase.md` + `ERD_Symbols_and_Notations.jpg` |

---

> ✨ *"Theory without practice is sterile. Practice without theory is blind."*  
> This repository merges both—designed for learners who build to understand, not just to execute.
