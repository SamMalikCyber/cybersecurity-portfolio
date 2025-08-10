# Apply More Filters in SQL

This mini project demonstrates how I used SQL comparison operators (`>`, `<`, `>=`, `<=`, `=`) and the `BETWEEN` operator to filter records by date, time, and unique IDs in MariaDB. These filters help zero in on relevant events quickly during investigations.

---

### Tools Used
- MariaDB shell
- SQL

---

### Commands Practiced and Their Output
```sql
-- Login attempts after Jan 15, 2023
SELECT *
FROM log_in_attempts
WHERE login_date > '2023-01-15';
-- Output: 112 login attempts after 2023-01-15

-- Login attempts between Feb 1 and Feb 7, 2023 (inclusive)
SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2023-02-01' AND '2023-02-07';
-- Output: 88 login attempts in that date range

-- Login attempts at exactly 09:30:00
SELECT *
FROM log_in_attempts
WHERE login_time = '09:30:00';
-- Output: 5 login attempts at 09:30:00

-- Details for a specific login attempt by ID
SELECT *
FROM log_in_attempts
WHERE login_id = 503;
-- Output: login_id 503 has login_date 2023-02-10
```

---

### Summary
I applied precise SQL filters to target login records by date (`>` and `BETWEEN`), exact time (`=`), and unique identifiers. Keeping the outputs noted under each query helps me recall context during reviews and interviews, and makes my queries faster and more focused in real investigations.
