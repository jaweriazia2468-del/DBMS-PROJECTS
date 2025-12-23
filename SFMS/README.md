# Scholarship Funding Management System (SFMS) 🎓

## 📌 Project Overview
The **SFMS** is an enterprise-grade backend database designed to automate the financial lifecycle of university scholarships. It manages the flow of capital from external donors (NGOs, Corporate CSR, Government) to student accounts, ensuring academic eligibility and financial transparency.

---

## 🛠️ Technical Portfolio
* **Database Architecture:** Relational schema designed in **Oracle SQL Developer**, normalized to **3rd Normal Form (3NF)** to ensure data integrity.
* **Logic & Automation:** Implemented **PL/SQL Triggers** to enforce business rules (e.g., minimum CGPA requirements) and automatic balance deductions.
* **DBA Operations:** Demonstrated full database portability by executing schema migrations using **Oracle Data Pump**.

---

## 📂 Repository Contents
| File | Description |
| :--- | :--- |
| `SFMS_CODE.sql` | Full DDL/DML script (Tables, Triggers, Views, and Sample Data). |
| `SFMS_ERD.pdf` | Entity-Relationship Diagram showing the logical data model. |
| `SFMS_EXPORT.dmp` | Binary export file created via **EXPDP** for schema migration. |

---

## 🚀 Key Features

### 1. Academic Accountability
The system links financial aid to student performance. Using **Triggers**, the database prevents scholarship allocation if a student's **CGPA** falls below the donor's threshold (e.g., 3.0).

### 2. Financial Custodianship
Every dollar is tracked. When an allocation is made, the system automatically updates the `REMAINING_BALANCE` in the `SCHOLARSHIP_FUNDS` table, preventing over-spending.

### 3. Schema Migration (Data Pump)
I have successfully migrated this database between environments using:
* **Directory Objects:** Configured secure physical storage paths in Oracle.
* **Export (EXPDP):** Generated a logical backup of the `SFMS` schema.
* **Import (IMPDP):** Restored the schema onto a separate instance, maintaining all constraints and triggers.

---

## 💡 How to Deploy
1. **SQL Script:** Run `SFMS_CODE.sql` in Oracle SQL Developer to build the schema.
2. **Data Pump:** Alternatively, use the `impdp` command to import the `.dmp` file directly into your Oracle instance.
