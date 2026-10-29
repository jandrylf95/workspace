# **SQL (Structured Query Language)**

## **Sublanguage**

| **Name** | **Purpouse** | **Key command** |
| :---: | :---: | :---: |
| **DDL (Data Definition Language)** | Defines and alters database structures/schemas. | `CREATE` , `ALTER` , `DROP` , `SHOW` |
| **DML (Data Manipulation Language)** | Manage and queries data inside table. | `SELECT` , `INSERT` , `UPDATE` , `DELETE` |
| **DCL (Data Control Language)** | Manage permissions and security access. | `GRANT` , `REVOKE` |
| **TCL (Transaction Control Language)** | Manage sets of database transactions | `COMMIT` , `ROLLBACK` |

<br><br>

## DDL 

#### 1. CREATE
Creates new database, tablet, views or indexes.  
```sql
CREATE TABLE Empleados (
    EmpleadoID INT PRIMARY KEY,
    Nombre VARCHAR(100),
    Salario DECIMAL(10,2)
);
```

#### 2. ALTER
Modifies the existing structure of an object.  
```sql
ALTER TABLE Empleados ADD Email VARCHAR(100)
```

#### 3. DROP
Permanently removes any database object.
```sql
DROP TABLE Empleados;

DROP VIEW view_name;

DROP SCHEMA schema_name;
DROP DATABASE db_name;
```

#### 4. TRUNCATE
Removes all rows from a table quickly, resetting its structure without deleting the table itself.
```sql
TRUNCATE TABLE table_name;
```

<br><br>

## DML
#### 1. SELECT
Retrieves or queries data from one or more tables.
```sql
SELECT column1, column2
FROM table_name
WHERE condition;
```
```sql
SELECT name_, salary FROM emp WHERE depId = 10;
```

#### 2. INSERT
Add new rows (tuplas) into a table.
```sql
INSERT INTO table_name (column1, column2)
VALUES (value1, value 2); 
```
- Specify column names is opcional.
- If you don't specify the column names, you must provide values for every single column in the table.
- You must list the values in the order that the columns where defined.  
Example:
```sql
INSERT INTO regions VALUES (5, `Australia`)
```
If you specify the columns:
```sql
INSERT INTO regions (region_id, region_name) 
VALUES (5, 'Australia');
```

#### 3. UPDATE
Modify especific values inside specific columns of a table.
```sql
UPDATE table_name
SET column1 = value1
WHERE condition;
```
Example
```sql
UPDATE regions
SET region_name = `Australia`
WHERE region_id = 5;
```

#### 4. DELETE
Remove specific rows from a table based on a condition.
```sql
DELETE FROM table_name
WHERE condition;
```
Example
```sql
DELETE FROM regions WHERE region_id = 5;
```

### **Important!**
- Always you need to include a `WHERE` when you are executing `UPDATE` or `DELETE`.
- If you don't use `WHERE` all rows in the table will be deleted.


<br><br>

## CONSTRAINT commands