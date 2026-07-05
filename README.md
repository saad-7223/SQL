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

## 📖 Entries

#### Q1: How can you retrieve all the information from the cd.facilities table?

**Link:** [pgexercises question link]

**My query:**
```sql
-- paste your query here
```

**What I learned:**

**Mistakes / gotchas:**
-

-
---

#### Q2: [Next exercise title]
**Link:**

**My query:**
```sql

```

-

**Mistakes / gotchas:**

---
## 🧠 Concept Cheat Sheet
As you learn something reusable, add a short note here so you don't have to dig through entries later.
| Concept | Quick note |
| `SELECT *` | Grabs all columns — fine for exploring, avoid in production code |
| `WHERE` | Filters rows before aggregation |
| `JOIN` | |
| `GROUP BY` | |
| `HAVING` | |

---

## 🏁 Reflections
A running space for bigger-picture thoughts as you move from basic → advanced.
- **[Date]** —


```markdown
#### Q3: List all customers
**Link:**

**My query:**
```sql
-- SELECT * FROM customers;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

#### Q4: Select specific columns
**Link:**

**My query:**
```sql
-- SELECT id, name, email FROM customers;
```

**What I learned:**
-

**Mistakes / gotchas:**
-

---

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
