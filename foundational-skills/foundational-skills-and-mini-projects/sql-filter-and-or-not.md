# Filter with AND, OR, and NOT

This mini project demonstrates how I used the `AND`, `OR`, and `NOT` operators in SQL to create more complex filters when querying a database. I applied these to investigate login activity and retrieve specific employee and machine data.

---

### Tools Used
- MariaDB shell
- SQL

---

### Commands Practiced and Their Output
```sql
-- Failed login attempts after 18:00
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
-- Output: 19 failed login attempts after business hours

-- Login attempts on 2022-05-08 or 2022-05-09
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
-- Output: 75 login attempts across both dates

-- Login attempts not from Mexico (MEX or MEXICO)
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
-- Output: 144 login attempts outside of Mexico

-- Marketing employees in the East building
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
-- Output: First username returned is elarson

-- Employees in Finance or Sales
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
-- Output: First Sales username is lrodriqu

-- Employees not in Information Technology
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
-- Output: 161 employees not in IT
```

---

### Summary
I practiced combining `AND`, `OR`, and `NOT` in SQL to apply multiple and exclusionary filters. This allowed me to narrow down login activity to specific dates, times, and locations, as well as retrieve targeted employee lists for department or building-based updates. These skills make investigations and updates faster and more precise.
