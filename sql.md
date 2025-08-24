# SQL

## Table of Contents

- [Introduction to Database ](#Introduction-to-Database)
- [Data Types](#data-types)
- [Operators](#operators)



## Introduction to Database

**Data** refers to any piece of information. It can be numbers, words, images, sounds, or any other information that a computer can store and process. Data can be raw or processed

A **database** is a structured collection of data that is organized in a way to facilitates efficient storage, retrieval, and manipulation of information.

A **Database Management System (DBMS)** is a software system that enables users to define, create, maintain, and manipulate databases. It provides an interface between the database and the users or applications, allowing them to access and manage data efficiently.

### Types of Databases
1. **Relational Databases (SQL databases)**: Relational databases(RDBMS) organize data into tables, where each table has rows and columns. These databases use structured query language (SQL) for defining and manipulating data.

*These are the following relational databases:*

    MySQL
    PostgreSQL
    Oracle (PL/SQL, programming language extension for Oracle Database)
    SQL Server
    SQLite
    MariaDB
    IBM Db2

2. **NoSQL Databases**: These databases are designed to handle large volumes of unstructured, semi-structured, or structured data. NoSQL provide flexible schema designs and often offer horizontal scalability.

*Types of NoSQL databases*

    1. Document databases: Store data in flexible, JSON-like documents.
    MongoDB
    Couchbase
    2. Key-value stores: Simplest NoSQL databases, storing data as key-value pairs.
    Redis
    Amazon DynamoDB.
    3. Column-family stores: Store data in columns rather than rows.
    Apache Cassandra
    HBase.
    4. Graph databases: Optimize for data with complex relationships.
    Neo4j
    Amazon Neptune.

**SQL**
Structured Query Language (SQL) is the standard language used to interact with relational databases.


### SQL Commands and Queries

#### 1. DDL (Data Definition Language): These commands are used to define the structure of database objects by creating, altering and dropping the database objects

| **Command** | **Description**                        | **Example Query** |
|-------------|----------------------------------------|-------------------|
| `CREATE`    | Creates a new table or database        | `CREATE TABLE employees (id INT, name VARCHAR(100));` |
| `ALTER`     | Modifies an existing table             | `ALTER TABLE employees ADD salary DECIMAL(10,2);` |
| `DROP`      | Deletes a table or database            | `DROP TABLE employees;` |
| `TRUNCATE`  | Removes all records from a table       | `TRUNCATE TABLE employees;` |

---

#### 2. DML (Data Manipulation Language): A relational database can be updated with new data using data manipulation language (DML) statements

| **Command** | **Description**                        | **Example Query** |
|-------------|----------------------------------------|-------------------|
| `SELECT`    | Retrieves data from one or more tables | `SELECT * FROM employees;` |
| `INSERT`    | Adds new data into a table             | `INSERT INTO employees (id, name) VALUES (1, 'John');` |
| `UPDATE`    | Modifies existing data in a table      | `UPDATE employees SET name = 'Jane' WHERE id = 1;` |
| `DELETE`    | Removes data from a table              | `DELETE FROM employees WHERE id = 1;` |

---

#### 3. DCL (Data Control Language): DCL commands manage user access to the database by granting or revoking permissions.

| **Command** | **Description**                        | **Example Query** |
|-------------|----------------------------------------|-------------------|
| `GRANT`     | Gives user access privileges           | `GRANT SELECT ON employees TO user1;` |
| `REVOKE`    | Removes user access privileges         | `REVOKE SELECT ON employees FROM user1;` |

---

#### 4. TCL (Transaction Control Language): TCL commands manage transactions in relational databases, ensuring data integrity and consistency. These commands are used to commit changes or roll back operations in case of errors.

| **Command**     | **Description**                          | **Example Query** |
|------------------|------------------------------------------|-------------------|
| `COMMIT`         | Saves all changes made during a transaction | `COMMIT;` |
| `ROLLBACK`       | Undoes changes since last COMMIT        | `ROLLBACK;` |
| `SAVEPOINT`      | Sets a point within a transaction        | `SAVEPOINT sp1;` |
| `SET TRANSACTION`| Sets properties for a transaction        | `SET TRANSACTION READ ONLY;` |

---

#### 5. DQL- Data Query Language: DQL is used to fetch data from the database

| **Clause / Command** | **Description**                        | **Example Query** |
|----------------------|----------------------------------------|-------------------|
| `JOIN`               | Combines rows from two or more tables  | `SELECT * FROM orders JOIN customers ON orders.customer_id = customers.id;` |
| `WHERE`              | Filters records                        | `SELECT * FROM employees WHERE salary > 50000;` |
| `GROUP BY`           | Groups rows sharing a property         | `SELECT department, COUNT(*) FROM employees GROUP BY department;` |
| `ORDER BY`           | Sorts the result-set                   | `SELECT * FROM employees ORDER BY name ASC;` |
| `HAVING`             | Filters groups based on a condition    | `SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 5;` |
| `DISTINCT`           | Returns unique values only             | `SELECT DISTINCT department FROM employees;` |
| `UNION`              | Combines results of two queries        | `SELECT name FROM customers UNION SELECT name FROM vendors;` |

## Data Types

### 1. Numeric Data Types

| **Data Type**    | **Description**                               | **Example**                  |
|------------------|-----------------------------------------------|------------------------------|
| `INT` / `INTEGER`| Whole numbers (positive or negative)          | `INT`, `INTEGER`             |
| `SMALLINT`       | Smaller range of integers                     | `SMALLINT`                   |
| `BIGINT`         | Larger range of integers                      | `BIGINT`                     |
| `DECIMAL(p, s)`  | Fixed-point number with precision and scale   | `DECIMAL(10,2)`              |
| `NUMERIC(p, s)`  | Same as DECIMAL                               | `NUMERIC(8,3)`               |
| `FLOAT(p)`       | Approximate numeric, floating-point           | `FLOAT(24)`                  |
| `REAL`           | Approximate numeric with lower precision      | `REAL`                       |
| `DOUBLE`         | Double precision floating-point               | `DOUBLE PRECISION`           |

---

### 2. String (Character) Data Types

| **Data Type**    | **Description**                                 | **Example**                 |
|------------------|-------------------------------------------------|-----------------------------|
| `CHAR(n)`        | Fixed-length string                             | `CHAR(10)`                  |
| `VARCHAR(n)`     | Variable-length string (max n characters)       | `VARCHAR(255)`              |
| `TEXT`           | Large text data (size varies by DBMS)           | `TEXT`                      |

---

### 3. Date and Time Data Types

| **Data Type**    | **Description**                      | **Example**        |
|------------------|--------------------------------------|--------------------|
| `DATE`           | Date (year, month, day)              | `'2025-08-24'`     |
| `TIME`           | Time (hour, minute, second)          | `'14:30:00'`       |
| `DATETIME`       | Date and time                        | `'2025-08-24 14:30:00'` |
| `TIMESTAMP`      | Date and time with time zone info    | `'2025-08-24 14:30:00+00'` |
| `YEAR`           | Year (used in MySQL)                 | `'2025'`           |

---

### 4. Boolean Type

| **Data Type**    | **Description**                      | **Example**       |
|------------------|--------------------------------------|-------------------|
| `BOOLEAN`        | Stores TRUE or FALSE                 | `TRUE`, `FALSE`   |
| `BOOL`           | Alias for BOOLEAN (MySQL/PostgreSQL) | `BOOL`            |

---

### 5. Binary Data Types

| **Data Type**    | **Description**                               | **Example**          |
|------------------|-----------------------------------------------|----------------------|
| `BINARY(n)`      | Fixed-length binary data                      | `BINARY(16)`         |
| `VARBINARY(n)`   | Variable-length binary data                   | `VARBINARY(256)`     |
| `BLOB`           | Binary Large Object (e.g., images, files)     | `BLOB`               |

---

### 6. Other Types (Vendor-Specific / Advanced)

| **Data Type**      | **Description**                               | **DBMS**              |
|--------------------|-----------------------------------------------|------------------------|
| `JSON`             | Stores JSON-formatted data                    | MySQL, PostgreSQL      |
| `UUID`             | Universally Unique Identifier                 | PostgreSQL             |
| `ENUM`             | String object with predefined values          | MySQL                  |
| `SET`              | A string object that can hold multiple values | MySQL                  |

## Operators

### 1. Arithmetic Operators

| **Operator** | **Description**              | **Example**              |
|--------------|------------------------------|--------------------------|
| `+`          | Addition                      | `SELECT 10 + 5;`         |
| `-`          | Subtraction                   | `SELECT 10 - 5;`         |
| `*`          | Multiplication                | `SELECT 10 * 5;`         |
| `/`          | Division                      | `SELECT 10 / 5;`         |
| `%`          | Modulus (remainder)           | `SELECT 10 % 3;`         |

---

### 2. Comparison Operators

| **Operator** | **Description**              | **Example**                        |
|--------------|------------------------------|------------------------------------|
| `=`          | Equal to                     | `WHERE salary = 5000`              |
| `!=` or `<>` | Not equal to                 | `WHERE department <> 'Sales'`      |
| `>`          | Greater than                 | `WHERE age > 30`                   |
| `<`          | Less than                    | `WHERE age < 30`                   |
| `>=`         | Greater than or equal to     | `WHERE age >= 18`                  |
| `<=`         | Less than or equal to        | `WHERE age <= 65`                  |
| `BETWEEN`    | Between a range of values    | `WHERE age BETWEEN 18 AND 30`      |
| `LIKE`       | Pattern matching             | `WHERE name LIKE 'A%'`             |
| `IN`         | Matches any value in a list  | `WHERE country IN ('US', 'UK')`    |
| `IS NULL`    | Checks for NULL value        | `WHERE address IS NULL`            |
| `IS NOT NULL`| Checks for NOT NULL value    | `WHERE email IS NOT NULL`          |

---

### 3. Logical Operators

| **Operator** | **Description**              | **Example**                                      |
|--------------|------------------------------|--------------------------------------------------|
| `AND`        | All conditions must be true  | `WHERE age > 18 AND city = 'New York'`          |
| `OR`         | At least one condition true  | `WHERE age < 18 OR age > 65`                    |
| `NOT`        | Negates a condition          | `WHERE NOT (status = 'active')`                 |

---

### 4. Bitwise Operators (Vendor-specific support)

| **Operator** | **Description**              | **Example**        |
|--------------|------------------------------|--------------------|
| `&`          | Bitwise AND                   | `SELECT 5 & 3;`     |
| `|`          | Bitwise OR                    | `SELECT 5 | 3;`     |
| `^`          | Bitwise XOR                   | `SELECT 5 ^ 3;`     |
| `~`          | Bitwise NOT (some DBs)        | `SELECT ~5;`        |
| `<<`         | Bitwise left shift            | `SELECT 5 << 1;`    |
| `>>`         | Bitwise right shift           | `SELECT 5 >> 1;`    |

---

### 5. Special Operators

| **Operator** | **Description**              | **Example**                                  |
|--------------|------------------------------|----------------------------------------------|
| `ANY`        | Compares value to any in subquery | `WHERE salary > ANY (SELECT salary FROM managers)` |
| `ALL`        | Compares value to all in subquery | `WHERE salary > ALL (SELECT salary FROM interns)` |
| `EXISTS`     | Checks if subquery returns rows   | `WHERE EXISTS (SELECT 1 FROM orders WHERE customer_id = c.id)` |

### 6. Compound Operators

| **Operator** | **Description**                        | **Equivalent To**             | **Example**                              |
|--------------|----------------------------------------|-------------------------------|------------------------------------------|
| `+=`         | Add and assign                         | `column = column + value`     | `SET salary += 1000;`                    |
| `-=`         | Subtract and assign                    | `column = column - value`     | `SET stock -= 5;`                        |
| `*=`         | Multiply and assign                    | `column = column * value`     | `SET price *= 1.05;`                     |
| `/=`         | Divide and assign                      | `column = column / value`     | `SET quantity /= 2;`                     |
| `%=`         | Modulus and assign                     | `column = column % value`     | `SET remainder %= 3;`                    |
| `&=`         | Bitwise AND and assign (T-SQL)         | `column = column & value`     | `SET flags &= 4;`                        |
| `|=`         | Bitwise OR and assign (T-SQL)          | `column = column \| value`    | `SET permissions |= 2;`                  |
| `^=`         | Bitwise XOR and assign (T-SQL)         | `column = column ^ value`     | `SET config ^= 1;`                       |

---


