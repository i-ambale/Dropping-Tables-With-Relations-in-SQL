# ⚡ Caveat on Dropping Tables with Relations

This project demonstrates proper techniques for managing database tables that have foreign key relationships, specifically focusing on how to safely drop tables that are being referenced by other tables.

---
## Key Concepts
Foreign Key Constraints
When dropping tables that are referenced by foreign keys in other tables, you must either:

1. Drop the dependent tables first

2. Temporarily disable foreign key checks

3. Use CASCADE options (where supported)

--
## 🧠 Learning Objectives
Understand how to drop a table that is referenced by another table using a foreign key.

Manage relational constraints properly before dropping tables.

Practice safe database management using MySQL Workbench and pymysql (for Python integration).

---
## ⚙️ Setup Requirements
MySQL Server installed locally.

MySQL Workbench installed.

Access to the united_nations database.

Python 3 (optional if connecting via pymysql).

⚠️ This notebook will NOT run on Google Colab due to local server connection requirements.

---
## 📋 Key Concepts Covered
Foreign Key Constraints: Prevent tables from being dropped if they are referenced by another table.

Safe Dropping: Proper procedure to avoid breaking relational integrity.

Disabling Foreign Key Checks temporarily when needed.

---
## 🗄️ Process Overview
1. Identify Relations
- Recognize which tables are linked via foreign keys.

2. Disable Foreign Key Checks (if necessary)
```
SET FOREIGN_KEY_CHECKS = 0;
```
3. Drop the Table Safely
```
DROP TABLE table_name;
```
4. Re-enable Foreign Key Checks
```
SET FOREIGN_KEY_CHECKS = 1;
```
🔥 Tip: Always backup your database before dropping tables!

---
## 🚀 How to Run
1. Open MySQL Workbench and connect to your local MySQL server.

2. Select the united_nations database.

3. Execute the SQL commands as per the process outlined.

4. (Optional) Connect via Python's pymysql for automation.

---
## 📸 Example SQL Snippet
```
-- Disable foreign key checks
SET FOREIGN_KEY_CHECKS = 0;

-- Drop the table
DROP TABLE Basic_services;

-- Re-enable foreign key checks
SET FOREIGN_KEY_CHECKS = 1;
```
---
👨‍💻 Author: Ibrahim Ambale

Developed as part of ExploreAI Academy coursework.

Crafted with care using MySQL, Python, and best database practices.
