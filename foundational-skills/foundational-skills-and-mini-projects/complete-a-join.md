# Complete a Join

This mini project demonstrates how I used SQL joins (`INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`) in MariaDB to combine data from multiple tables. This allowed me to link related records across machines, employees, and login attempts for investigation purposes.

---

### Tools Used
- MariaDB shell
- SQL

---

### Commands Practiced and Their Output
```sql
-- Inner join: match employees to their machines
SELECT *
FROM machines
INNER JOIN employees ON machines.device_id = employees.device_id;
-- Output: 185 rows returned

-- Left join: all machines and their assigned employees
SELECT *
FROM machines
LEFT JOIN employees ON machines.device_id = employees.device_id;
-- Output: last username returned is NULL

-- Right join: all employees and their assigned machines
SELECT *
FROM machines
RIGHT JOIN employees ON machines.device_id = employees.device_id;
-- Output: last username returned is areyes

-- Inner join: employees with their login attempts
SELECT *
FROM employees
INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;
-- Output: 200 rows returned
```

---

### Summary
I practiced joining related tables in SQL to connect data across machines, employees, and login logs. Using `INNER JOIN` gave me only matching records, `LEFT JOIN` kept all machines regardless of assigned employees, and `RIGHT JOIN` kept all employees regardless of assigned machines. These join techniques are key for investigations when data is spread across multiple tables. I have to admit that these might be simpler concepts, but the combination of these commands, working for a real organization, and presenting information that I've gathered from these procedures is one of my weaknesses. I will be working on this a lot, especially if you want me to!
