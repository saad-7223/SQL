# SQL Practice Journal — pgexercises.com

Documenting my progress through [pgexercises.com](https://pgexercises.com), from basic queries to advanced SQL concepts.

## 📌 How to use this journal
Each exercise gets an entry with: the question, my query, what I learned, and any mistakes I made along the way. Mistakes are the most valuable part — keep them in, don't delete them.

## 🗂️ Progress Tracker

| Section | Status | Notes |
|---|---|---|
| Basics (SELECT) | ⬜ Not started | |
| Basics (WHERE, filtering) | ⬜ Not started | |
| Aggregates | ⬜ Not started | |
| Joins | ⬜ Not started | |
| Modifying Data (INSERT/UPDATE/DELETE) | ⬜ Not started | |
| Recursive Queries | ⬜ Not started | |

Update status as: ⬜ Not started → 🟡 In progress → ✅ Done

---

## 📖 CASE OPeration

#### Q1: How can you produce a list of facilities, with each labelled as 'cheap' or 'expensive' depending on if their monthly maintenance cost is more than $100? Return the name and monthly maintenance of the facilities in question. 

**Link:** https://pgexercises.com/questions/basic/classify.html

**My query:**
```sql
select name , 
case 
    when monthlymaintenance < 100 then 'cheap'
    else 'expensive'
end as cost
from cd.facilities
```

**What I learned:**

**Mistakes / gotchas:**
- caseing in SQL
- Syntax : 
    CASE
    <br>    WHEN condition1 THEN result1
    <br>    WHEN condition2 THEN result2
    <br>    ...
    <br>    ELSE default_result
    <br>END
---
## 📖 UNION Operation

#### Q2: You, for some reason, want a combined list of all surnames and all facility names. Yes, this is a contrived example. Produce that list!

**Link: https://pgexercises.com/questions/basic/union.html**

**My query:**
```sql
select surname from cd.members
union 
select name from cd.facilities;
```
**Mistakes / gotchas:**
- Learned union operator 
- SELECT column1, column2, ...
<br>FROM table1
<br>[WHERE condition]
<br>UNION
<br>SELECT column1, column2, ...
<br>FROM table2
<br>[WHERE condition];


## 📖 SubQuery in SQL

#### Q3: You'd like to get the first and last name of the last member(s) who signed up - not just the date. How can you do that?
**Link: https://pgexercises.com/questions/basic/agg2.html**

**My query:**
```SQL
select firstname , surname , joindate
from cd.members
where joindate = (select max(joindate) from cd.members);
```

**What I learned:**
- Learned how query inside a query works for complex extraction of data
- SELECT column_name
FROM table_name<br>
WHERE column_name operator (SELECT column_name FROM table_name WHERE condition);   

## 📖 Inner Join

#### Q4: How can you produce a list of the start times for bookings by members named 'David Farrell'?
**Link: https://pgexercises.com/questions/joins/simplejoin.html**

**My query:**
```sql
select b.starttime 
from cd.bookings as b 
inner join cd.members as m 
on m.memid = b.memid
where 
m.surname = 'Farrell' and m.firstname = 'David';
```

**What I learned:**
- learned the syntax and when to use this operation 
- Use when need to search through 2 tables
```
    SELECT table1.column1, table2.column2
    FROM table1
    INNER JOIN table2 
    ON table1.common_column = table2.common_column;   
```

## 📖 Entries
#### Q5: Filter rows with WHERE
**Link:**

**My query:**
```sql
-- SELECT * FROM orders WHERE amount > 100;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q6: Use ORDER BY
**Link:**

**My query:**
```sql
-- SELECT * FROM products ORDER BY created_at DESC;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q7: Aggregate with COUNT
**Link:**

**My query:**
```sql
-- SELECT COUNT(*) FROM orders;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q8: GROUP BY example
**Link:**

**My query:**
```sql
-- SELECT customer_id, SUM(amount) FROM orders GROUP BY customer_id;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q9: JOIN two tables
**Link:**

**My query:**
```sql
-- SELECT o.id, c.name FROM orders o JOIN customers c ON o.customer_id = c.id;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q10: LEFT JOIN to keep all left rows
**Link:**

**My query:**
```sql
-- SELECT p.id, c.name FROM products p LEFT JOIN categories c ON p.category_id = c.id;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q11: UPDATE statement
**Link:**

**My query:**
```sql
-- UPDATE users SET last_login = now() WHERE id = 1;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q12: DELETE with caution
**Link:**

**My query:**
```sql
-- DELETE FROM sessions WHERE expires_at < now();
```

**What I learned:**
-

**Mistakes / gotchas:**
-
#### Q: [Exercise title]
**Link:**

**My query:**
​```sql

​```

**What I learned:**
-

**Mistakes / gotchas:**
-
```
