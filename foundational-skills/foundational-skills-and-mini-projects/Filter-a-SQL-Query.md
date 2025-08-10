# Filter a SQL Query

This mini project demonstrates how I applied filters to SQL queries in MariaDB to pull only the data I needed. I used exact matches with `WHERE` and pattern matching with `LIKE` to narrow results for machines, employees, and departments.

---

### Tools Used
- MariaDB shell
- SQL

---

### Commands Practiced and Their Output
```sql
-- List machines and their operating systems
SELECT device_id, operating_system
FROM machines;
-- Output: 200 rows, including:
-- a184b775c707 | OS 1
-- a192b174c940 | OS 2
-- a305b818c708 | OS 3

-- Machines running OS 2
SELECT device_id, operating_system
FROM machines
WHERE operating_system = 'OS 2';
-- Output: 80 rows, all with OS 2

-- Employees in Finance
SELECT *
FROM employees
WHERE department = 'Finance';
-- Output: First row employee_id = 1003

-- Employees in Sales
SELECT *
FROM employees
WHERE department = 'Sales';
-- Output: 33 employees in Sales

-- Employee in South-109
SELECT *
FROM employees
WHERE office = 'South-109';
-- Output: User ID = jlansky

-- All employees in the South building
SELECT *
FROM employees
WHERE office LIKE 'South%';
-- Output: First employee listed is in the Finance department
```

---

### Summary
I practiced filtering SQL results using `WHERE` for exact values and `LIKE` for simple patterns. This makes it faster to find relevant data (who’s in which department, which machines need attention) and supports quick checks during investigations.

