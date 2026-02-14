# SQL_QucikRevise
Quick Revise of SQL Queries.

---

## 🔑 Core SQL Query Types

### 1. **Data Retrieval (SELECT)**
- `SELECT column1, column2 FROM table;`
- Filtering: `WHERE condition`
- Sorting: `ORDER BY column ASC/DESC`
- Limiting: `LIMIT n` (MySQL/Postgres) or `TOP n` (SQL Server)

### 2. **Data Modification**
- Insert:  
  `INSERT INTO table (col1, col2) VALUES (val1, val2);`
- Update:  
  `UPDATE table SET col1 = val1 WHERE condition;`
- Delete:  
  `DELETE FROM table WHERE condition;`

### 3. **Joins**
- Inner Join:  
  `SELECT a.col, b.col FROM tableA a INNER JOIN tableB b ON a.id = b.id;`
- Left Join: keeps all rows from left table.  
- Right Join: keeps all rows from right table.  
- Full Join: keeps all rows from both tables.

### 4. **Aggregation**
- `COUNT(), SUM(), AVG(), MIN(), MAX()`
- Grouping:  
  `SELECT dept, COUNT(*) FROM employees GROUP BY dept;`
- Filtering groups:  
  `HAVING COUNT(*) > 5`

### 5. **Subqueries**
- Inline:  
  `SELECT name FROM employees WHERE dept_id IN (SELECT id FROM departments WHERE location='NY');`
- Correlated: depends on outer query.

### 6. **Set Operations**
- `UNION` (removes duplicates)  
- `UNION ALL` (keeps duplicates)  
- `INTERSECT`  
- `EXCEPT` / `MINUS`

### 7. **DDL (Data Definition)**
- Create:  
  `CREATE TABLE employees (id INT PRIMARY KEY, name VARCHAR(100));`
- Alter:  
  `ALTER TABLE employees ADD COLUMN salary DECIMAL;`
- Drop:  
  `DROP TABLE employees;`

### 8. **Advanced Features**
- Window Functions:  
  `ROW_NUMBER(), RANK(), DENSE_RANK(), LAG(), LEAD()`
- CTEs (Common Table Expressions):  
  `WITH temp AS (SELECT ...) SELECT * FROM temp;`
- Transactions:  
  `BEGIN; ... COMMIT;` or `ROLLBACK;`

---

## ⚡ Quick Tips
- Always use `WHERE` with `UPDATE` and `DELETE` to avoid affecting all rows.
- Prefer `JOIN` over subqueries for readability and performance.
- Use indexes wisely to speed up queries.
- Normalize tables for consistency, but denormalize for performance when needed.

---



