


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

> **Note**: Microsoft does not use "SSMS 21" naming. The latest stable version is **SSMS 19.x** (fully compatible with SQL Server 2022). This guide covers the current official release.

#### Installation Steps:
1. **Download SSMS**  
   → Official download: https://aka.ms/ssmsfullsetup  
   → Click **"Download SQL Server Management Studio (SSMS)"**

2. **Run Installer**  
   → Locate `SSMS-Setup-ENU.exe` → Right-click → **Run as administrator**  
   → Accept license terms → Click **Install**

3. **Complete Setup**  
   → Wait 5–10 minutes for installation  
   → Click **Close** → *Recommended*: Restart your computer

4. **Verify Installation**  
   → Press `Win + S` → Type "SSMS" → Open application  
   → Check version: `Help → About` → Should display **v19.x.x**

---

### ✅ Step 2: Connect to SQL Server

| Scenario | Server Name | Authentication | Notes |
|----------|-------------|----------------|-------|
| **Local default instance** | `localhost` or `.` | Windows Authentication | Requires SQL Server installed locally |
| **SQL Server Express** | `localhost\SQLEXPRESS` | Windows Authentication | Default instance name for Express edition |

> 💡 **Don't have SQL Server installed?**  
> → Download free **SQL Server 2022 Express**: https://www.microsoft.com/sql-server/sql-server-downloads  
> → During install: Select "Basic" → Note your instance name → Connect via SSMS using that name

---

### ✅ Step 3: Restore Practice Databases

```sql
-- Method 1: Restore from .bak file (recommended)
-- In SSMS: Right-click Databases → Restore Database → Device → Browse → Select .bak file → OK

-- Method 2: Run initialization script
-- Open init-sqlserver-mydatabase.sql → Click "Execute" (F5)
```

> 📌 **Pro Tip**: Keep `Execution order.pdf` open while practicing—it reveals the *logical* query execution sequence (`FROM` → `WHERE` → `GROUP BY` → `HAVING` → `SELECT` → `ORDER BY`), which differs from written syntax order.

---

## 🧭 Recommended Learning Path

1. **Theory First**  
   → Read `roadmap.md` → Study `Complete_DBMS_Notes.md` → Review visual aids

2. **Validate Understanding**  
   → Solve problems in `Theoretical Exercises/` *before* writing code

3. **Hands-On Practice**  
   → Install SSMS → Restore `.bak` files → Experiment using PDF guides

4. **Extend Knowledge**  
   → Explore analytics/warehouse projects in `resources/`

---

## 🙏 Credits & Acknowledgements

The Datawithbaraa was created through immersive learning inspired by **[Datawithbaraa](https://www.youtube.com/@Datawithbaraa)**. His clear, structured approach to database concepts and SQL practice provided the foundational framework for this learning journey. Thank you for making complex topics accessible and actionable.

---

## 📜 License

```
MIT License

Copyright (c) 2026 Ahnaf Nasim

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
---

## 📌 Quick Reference Cheat Sheet

| Concept | Files to Pair |
|---------|---------------|
| **Keys** | `Key.md` + `typesOfKeys.jpg` + `key.jpg` |
| **Joins** | `relationshipVSjoin.md` + `img-type-of-joins.png` + `Join.pdf` |
| **Normalization** | `normalization1.png` → `normalization2.png` (study sequentially) |
| **ER Diagrams** | `ER-diagram-relationalDatabase.md` + `ERD_Symbols_and_Notations.jpg` |

---

> ✨ *"Theory without practice is sterile. Practice without theory is blind."*  
> This repository merges both—designed for learners who build to understand, not just to execute.
