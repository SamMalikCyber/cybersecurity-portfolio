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

-- Machines running OS 2
SELECT device_id, operating_system
FROM machines
WHERE operating_system = 'OS 2';

-- Employees in Finance
SELECT *
FROM employees
WHERE department = 'Finance';

-- Employees in Sales
SELECT *
FROM employees
WHERE department = 'Sales';

-- Employee in South-109
SELECT *
FROM employees
WHERE office = 'South-109';

-- All employees in the South building
SELECT *
FROM employees
WHERE office LIKE 'South%';
```

---

### Summary
I practiced filtering SQL results using `WHERE` for exact values and `LIKE` for simple patterns. This makes it faster to find relevant data (who’s in which department, which machines need attention) and supports quick checks during investigations.
