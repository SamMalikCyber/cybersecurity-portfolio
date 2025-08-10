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
-- Output: All 200 rows from the machines table, including device_id, OS, email_client, patch date, and employee ID.

-- Select specific columns
SELECT device_id, email_client
FROM machines;
-- Output: Device IDs and email client types. Third row showed Email Client 2.

-- Select device ID, OS, and patch date
SELECT device_id, operating_system, OS_patch_date
FROM machines;
-- Output: Device IDs with their OS and patch dates. First entry had patch date 2021-09-01.

-- Check login locations
SELECT event_id, country
FROM log_in_attempts;
-- Output: Countries for all login attempts. None from Australia.

-- Check logins outside working hours
SELECT username, login_date, login_time
FROM log_in_attempts;
-- Output: Usernames with date/time. Fifth row username was 'jrafael'.

-- View all login attempts
SELECT * 
FROM log_in_attempts;
-- Output: Full login_attempts table.

-- Order login attempts by date
SELECT * 
FROM log_in_attempts
ORDER BY login_date;
-- Output: First record was 'ivelasco' on 2022-05-08.

-- Order login attempts by date and time
SELECT * 
FROM log_in_attempts
ORDER BY login_date, login_time;
-- Output: First record was 'bsand' at 00:19:11 on 2022-05-08.
```

---

### Summary
This task gave me hands-on practice with running SQL queries to pull information from multiple tables in a database. I selected specific columns, retrieved all records, and used `ORDER BY` to sort results by date and time. These skills are essential for quickly finding and organizing data when investigating security events or maintaining system records. Digital forensics is a field that particularly interests me, so this is an area that I am focusing on.
