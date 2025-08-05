# Data-Insertion-and-Handling-Nulls

**Objective:**
Practice SQL operations like inserting, updating, and deleting records, and learn how to handle NULL values effectively.

**Tool Used:**
MySQL Workbench

**Database Overview**

Database Name: employees

Table: employees_data

Fields:

id (INT, Primary Key)

name (VARCHAR)

age (INT)

salary (INT)

**Inserted Records:**

Added 13 employees using INSERT INTO.

Included cases with NULL salary and NULL age to practice null handling.

**Update Operations:**

Increased salary by ₹10,000 for employees earning less than ₹30,000.

Replaced NULL salary with ₹25,000.

Replaced NULL age with 27.

**Delete Operation:**

Deleted employee with id = 9 (Veldora).

**SQL Snippets**

-- Increase salary conditionally

UPDATE employees_data
SET salary = salary + 10000
WHERE salary < 30000;

-- Handle NULL values

UPDATE employees_data
SET salary = 25000
WHERE salary IS NULL;

UPDATE employees_data
SET age = 27
WHERE age IS NULL;

-- Delete a record

DELETE FROM employees_data
WHERE id = 9;
