# SQL Basics Cheat Sheet

This document provides a quick reference for basic SQL commands to help you interact with and manage databases.

---

## 1. **Database Operations**

- **Create a new database:**
  ```sql
  CREATE DATABASE database_name;
  ```

- **Use a database:**
  ```sql
  USE database_name;
  ```

- **Delete a database:**
  ```sql
  DROP DATABASE database_name;
  ```

---

## 2. **Table Operations**

- **Create a new table:**
  ```sql
  CREATE TABLE table_name (
      column1 datatype constraints,
      column2 datatype constraints,
      ...
  );
  ```

- **View table structure:**
  ```sql
  DESCRIBE table_name;
  ```

- **Delete a table:**
  ```sql
  DROP TABLE table_name;
  ```

- **Truncate a table (delete all rows):**
  ```sql
  TRUNCATE TABLE table_name;
  ```

---

## 3. **CRUD Operations**

### Create (Insert Data):
- **Insert a single row:**
  ```sql
  INSERT INTO table_name (column1, column2, ...) 
  VALUES (value1, value2, ...);
  ```

- **Insert multiple rows:**
  ```sql
  INSERT INTO table_name (column1, column2, ...) 
  VALUES 
      (value1a, value2a, ...),
      (value1b, value2b, ...);
  ```

### Read (Retrieve Data):
- **Select all rows and columns:**
  ```sql
  SELECT * FROM table_name;
  ```

- **Select specific columns:**
  ```sql
  SELECT column1, column2 FROM table_name;
  ```

- **Filter rows with conditions:**
  ```sql
  SELECT * FROM table_name WHERE condition;
  ```

- **Order results:**
  ```sql
  SELECT * FROM table_name ORDER BY column1 [ASC|DESC];
  ```

### Update (Modify Data):
- **Update rows:**
  ```sql
  UPDATE table_name
  SET column1 = value1, column2 = value2
  WHERE condition;
  ```

### Delete (Remove Data):
- **Delete specific rows:**
  ```sql
  DELETE FROM table_name WHERE condition;
  ```

- **Delete all rows:**
  ```sql
  DELETE FROM table_name;
  ```

---

## 4. **Constraints**
- **Primary Key:** Ensures uniqueness for a column.
  ```sql
  CREATE TABLE table_name (
      id INT PRIMARY KEY,
      name VARCHAR(50)
  );
  ```

- **Foreign Key:** Creates a relationship between two tables.
  ```sql
  CREATE TABLE child_table (
      id INT,
      parent_id INT,
      FOREIGN KEY (parent_id) REFERENCES parent_table(id)
  );
  ```

- **Not Null:** Ensures a column cannot have NULL values.
  ```sql
  CREATE TABLE table_name (
      id INT NOT NULL
  );
  ```

---

## 5. **Joins**

- **Inner Join:**
  ```sql
  SELECT * 
  FROM table1
  INNER JOIN table2 ON table1.column = table2.column;
  ```

- **Left Join:**
  ```sql
  SELECT * 
  FROM table1
  LEFT JOIN table2 ON table1.column = table2.column;
  ```

- **Right Join:**
  ```sql
  SELECT * 
  FROM table1
  RIGHT JOIN table2 ON table1.column = table2.column;
  ```

- **Full Outer Join:**
  ```sql
  SELECT * 
  FROM table1
  FULL OUTER JOIN table2 ON table1.column = table2.column;
  ```

---

## 6. **Aggregate Functions**

- **Count rows:**
  ```sql
  SELECT COUNT(*) FROM table_name;
  ```

- **Find maximum value:**
  ```sql
  SELECT MAX(column_name) FROM table_name;
  ```

- **Find minimum value:**
  ```sql
  SELECT MIN(column_name) FROM table_name;
  ```

- **Calculate average:**
  ```sql
  SELECT AVG(column_name) FROM table_name;
  ```

- **Sum values:**
  ```sql
  SELECT SUM(column_name) FROM table_name;
  ```

---

## 7. **Miscellaneous**

- **Alias (rename columns or tables):**
  ```sql
  SELECT column_name AS alias_name FROM table_name;
  ```

- **Limit the number of rows returned:**
  ```sql
  SELECT * FROM table_name LIMIT 10;
  ```

- **Create an index:**
  ```sql
  CREATE INDEX index_name ON table_name (column_name);
  ```

- **Delete an index:**
  ```sql
  DROP INDEX index_name;
  ```

---

Keep this cheat sheet handy while working with SQL for quick reference. Happy querying!
