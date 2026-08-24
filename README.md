# MySQL_Clauses-and-Joins

🗃️ Employee Database — MySQL DML Project

A Data Analyst assignment focused on designing and managing an Employee Database using MySQL.

DML: populating the tables and querying them with DISTINCT, aliases, WHERE, ORDER BY, LIMIT, aggregate functions, GROUP BY, HAVING, and all three join types.

📌 Problem Statement

As a Data Analyst, the company requires an Employee Database to store and manage information related to employees, departments, and locations. The goal is to design this database using MySQL DDL commands, while enforcing appropriate constraints to ensure data integrity and consistency.

🧩 Schema Overview

Table	Key Attributes

Departments_Info	department_id (PK), department_name
Locations	location_id (PK, auto-increment), location_name
Employees	employee_id (PK), employee_name, gender, age, hire_date, designation, salary, department_id (FK), location_id (FK), email

⚙️ What employee_database.sql Does

The script is organized into six clearly commented sections, meant to be run top to bottom:

Run these after employee_database.sql so the constrained schema already exists.

employee_data_insert.sql

Populates Departments_Info (5 departments), Locations (5 locations), and Employees (15 employees) with deliberately varied data so every query below returns meaningful, non-empty results:

One employee (Priya M) has a missing designation — used to test the UPDATE ... WHERE designation IS NULL task.

One employee (Gopal K) has no department_id — used to show the difference between INNER JOIN and LEFT JOIN.

One department (Legal) and one location (Hyderabad) have zero employees — used to prove LEFT JOIN / RIGHT JOIN return NULL instead of silently dropping the row.

dml_queries.sql

Contains every query task from the assignment, grouped and commented into sections:

Section	Task
A. Distinct Values	Distinct salaries
B. Alias (AS)	age → Employee_Age, salary → Employee_Salary
C. WHERE Clause & Operators	Salary > ₹50000 & hired before 2016-01-01; find & fill missing designation
D. ORDER BY	Sorted by department_id ASC, salary DESC
E. LIMIT	First 5 employees hired in 2018
F. Aggregate Functions	Sum of Finance salaries; minimum age
G. GROUP BY	Max salary per location; avg salary per %Analyst% designation
H. HAVING	Departments with < 3 employees; locations with avg female age < 30
I. Joins	INNER JOIN, LEFT JOIN, RIGHT JOIN

🛠️ Tech Stack
Database: MySQL 8.0+
Tooling: MySQL Workbench / MySQL CLI

👤 Author

Data Analyst Assignment — Employee Database DDL & Constraints Project.
