# Perform an SQL Query

This mini project demonstrates how I used SQL commands to retrieve specific information from a database and organize the results using the `ORDER BY` keyword.

---

### Tools Used
- MariaDB shell
- SQL

---

### Commands Practiced and Their Output
```sql
-- Retrieve all data from machines table
SELECT * 
FROM machines;

-- Select specific columns
SELECT device_id, email_client
FROM machines;

-- Select device ID, OS, and patch date
SELECT device_id, operating_system, OS_patch_date
FROM machines;

-- Check login locations
SELECT event_id, country
FROM log_in_attempts;

-- Check logins outside working hours
SELECT username, login_date, login_time
FROM log_in_attempts;

-- View all login attempts
SELECT * 
FROM log_in_attempts;

-- Order login attempts by date
SELECT * 
FROM log_in_attempts
ORDER BY login_date;

-- Order login attempts by date and time
SELECT * 
FROM log_in_attempts
ORDER BY login_date, login_time;
```

---

### Summary
This task gave me hands-on practice with running SQL queries to pull information from multiple tables in a database. I selected specific columns, retrieved all records, and used `ORDER BY` to sort results by date and time. These skills are essential for quickly finding and organizing data when investigating security events or maintaining system records. Digital forensics is a field that also interests me, so this is an area that I am focusing on.
