# WHAT WE DID THIS WEEK (web-dev)

<details>
<summary><b>Template</b></summary>

## Week 3 

### Notes

#### Tutorship

- 
- 

#### Didactic guide

---
### Done this week
1. 

### Pending Work
```
- [ ] 
- [ ] 
```
---
---
</details>

---

### Resources
[Web-Dev PHP Course](https://www.mclibre.org/consultar/php/ "Introductory course on web page programming in PHP")

<br>

## Week 4

### Notes

#### Tutorship
`PHP` process the request and `MySQL` stores and returns the data.

This week tutorship was mostly about SQL

- PK (Primary key): Assign an unique id to every row.
- `IF NOT EXISTS` check if there is another db with the same name, before the creation.
- `USE` selects the schema/database that we want to interact with.
- When we have a field named Cedula it should be as `VARCHAR()`, because there are cedulas that stars with 0 and if we use `INT` the first 0 will be dropped.
- Four operations: `CRUD (CREATE, READ, UPDATE, DELETE)`
- Most used commands: `CREATE DATABASE`, `SHOW DATABASE`, `USE`, `CREATE TABLE`, `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
- **phpMyAdmin:**  It's an interface to admin the database.
     - **Allow:**
     - Allows create db and tables.
     - Explore records.
     - Execute SQL queries.
     - Import and export data.


***Common data types:*** 
| Type | Detail |
| :--- | :--- |
| **VARCHAR(n)** | Text|  
| **INT** | Integer numbers|  
| **DECIMAL(p,s)** | Decimal numbers |
| **DATE** | Dates |
| **DATETIME** | Date and time |

***Constraints:***
| Type | Detail |
| :--- | :--- |
| **PRIMARY KEY** | id of the row. |
| **NOT NULL** | Mandatory data |
| **UNIQUE** | Avoid duplicates |
| **FOREIGN KEY** | Relation between tables |

Example of connection with local variables `PHP` /
`PHP` connects with MySQL through `PDO`
```php
<?php
$pdo = new PDO (
    'mysql:host=localhost;dbname=tienda_web;charset=utf8mb4' ,
    $usuario,
    $contrasena
);
$pdo->setAtribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
```

Queries from `PHP`:
```php
$sql = 'SELECT nombre, apellido FROM persona
        WHERE cedula = cedula';
$stmt = $pdo->prepare ($sql);
$stmt->execute(['cedula' => $cedula]);
$persona = $stmt->fetch(PDO::FETCH_ASSOC);
```


#### Didactic guide

Unit 3: PHP with MySQL

`phpMyAdmin` to administrate db. (MySQL / MariaDB)
[phpMyAdmin Guide](https://www.mclibre.org/consultar/php/otros/xampp-phpmyadmin.html "")

- Creation of data base through Terminal
- Data base lists `SHOW DATABASE`
- Table creation
- SQL data manipulation


---
### Done this week 4
1. Environment already created.
1. Finished de tutorship and notes about it.

### Pending Work

```
- [] Check tutorship and take notes about the week 3.
- []  
```
---
---