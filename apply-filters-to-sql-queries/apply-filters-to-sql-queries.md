# Apply Filters to SQL Queries

## Project Description
My organization is tightening security around employee logins and machines. I pulled targeted data from the `employees` and `log_in_attempts` tables using SQL filters. Below are the specific queries I used and why.

---

## Retrieve after hours failed login attempts
A potential incident occurred after business hours (after `18:00`). I filtered for failed attempts that happened after that time.

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
  AND success = FALSE;
```

This returns only unsuccessful attempts after `18:00` so we can review them first.  

![After-hours failed logins](apply-filters-to-sql-queries/images/after-hours-failed-logins.png)

---

## Retrieve login attempts on specific dates
A suspicious event happened on `2022-05-09`. I pulled logins from that day and the day before.

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09'
   OR login_date = '2022-05-08';
```

Using `OR` captured both dates in one pass.  

![Specific dates logins](apply-filters-to-sql-queries/images/logins-specific-dates.png)

---

## Retrieve login attempts outside of Mexico
The dataset stores Mexico as `MEX` or `MEXICO`. I excluded both with a single pattern.

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

`LIKE 'MEX%'` matches both forms; `NOT` flips the condition so we see non-Mexico activity.  

![Not Mexico logins](apply-filters-to-sql-queries/images/logins-not-mexico.png)

---

## Retrieve employees in Marketing
We needed Marketing users **in the East building** for an update.

```sql
SELECT *
FROM employees
WHERE department = 'Marketing'
  AND office LIKE 'East%';
```

`AND` ensures both the department and building criteria are true.  

![Marketing East](apply-filters-to-sql-queries/images/marketing-east.png)

---

## Retrieve employees in Finance or Sales
Separate update for Finance **or** Sales.

```sql
SELECT *
FROM employees
WHERE department = 'Finance'
   OR department = 'Sales';
```

`OR` returns anyone in either department.  

![Finance or Sales](apply-filters-to-sql-queries/images/finance-or-sales.png)

---

## Retrieve all employees not in IT
Final pass: everyone **not** in Information Technology.

```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

This excludes IT so we can focus updates on the rest of the org.

![Not IT](apply-filters-to-sql-queries/images/not-it.png)

---

## Summary
I used `AND`, `OR`, and `NOT` to target the exact records needed, plus `LIKE 'East%'` and `LIKE 'MEX%'` to handle building tags and country variants. These filters narrowed big tables into lists that can be used for investigation and system updates without pulling unnecessary data.
