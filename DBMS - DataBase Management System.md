**DBMS - DataBase Management System**



**Definition-** A DBMS is a collection of programs that enables users to create and maintain a database. It provides an interface between the user and the data.

A software system used to store, retrieve, manage, and manipulate data efficiently in a database.

**Data-** Raw facts or figures that do not have any meaning by themselves.

Example: "John", "22", "CSE" (individually meaningless)

**Information →** Processed, meaningful data

**📝 Types of Databases :**



**1. Relational Database (RDBMS)**

→ Data stored in tables (rows \& columns).

→ Uses SQL for operations.

Examples: MySQL, Oracle, PostgreSQL, SQL Server

Features:

1.Normalization

2.Primary \& Foreign keys

3.Strong consistency

**📝 JSON Tabular Form:**

JSON = JavaScript Object Notation

Definition: JSON tabular form means representing table-like data (rows \& columns) using JSON objects and arrays.

**📝 Query**

A query is a request for information from a database.

It is written using SQL (Structured Query Language).



 **CODE :**

CREATE TABLE STUDENTS(

studentsID varchar(100),Age, int, City varchar(100));





CREATE TABLE PERSONALINFO (

&nbsp;   PERSONALINFOID VARCHAR(100),

&nbsp;   name VARCHAR(100),

&nbsp;   age INT,

&nbsp;   location VARCHAR(100)

);



INSERT INTO PERSONALINFO (PERSONALINFOID, name, age, location)

VALUES

('1', 'Aman', 19, 'Gurugram'),

('2', 'Ritik', 25, 'Delhi');

select \* FROM PERSONALINFO;



desc PERSONALINFO;



select name from PERSONALINFO;



**TABLE :**



CREATE TABLE PERSONALINFO (

&nbsp;   PERSONALINFOID VARCHAR(100),

&nbsp;   name VARCHAR(100),

&nbsp;   age INT,

&nbsp;   location VARCHAR(100)

);



INSERT INTO PERSONALINFO (PERSONALINFOID, name, age, location)

VALUES

('1', 'Aman', 19, 'Gurugram'),

('2', 'Ritik', 25, 'Delhi');

select \* FROM PERSONALINFO;



desc PERSONALINFO;



select name from PERSONALINFO where PERSONALINFOID >= 1;

**Output:**



+----------------+-------+------+----------+

| PERSONALINFOID | name  | age  | location |

+----------------+-------+------+----------+

| 1              | Aman  |   19 | Gurugram |

| 2              | Ritik |   25 | Delhi    |

+----------------+-------+------+----------+

+----------------+--------------+------+-----+---------+-------+

| Field          | Type         | Null | Key | Default | Extra |

+----------------+--------------+------+-----+---------+-------+

| PERSONALINFOID | varchar(100) | YES  |     | NULL    |       |

| name           | varchar(100) | YES  |     | NULL    |       |

| age            | int          | YES  |     | NULL    |       |

| location       | varchar(100) | YES  |     | NULL    |       |

+----------------+--------------+------+-----+---------+-------+

+-------+

| name  |

+-------+

| Aman  |

| Ritik |

+-------+



**UPDATE COMMAND**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Dave', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');



-- fetch 

-- SELECT \* FROM EMPLOYEE WHERE dept = 'Sales';

update EMPLOYEE set name='Aman' where empId = 2;

SELECT \* FROM EMPLOYEE;

**Output:**



+-------+-------+------------+

| empId | name  | dept       |

+-------+-------+------------+

|     1 | Clark | Sales      |

|     2 | Aman  | Accounting |

|     3 | Ava   | Sales      |

+-------+-------+------------+

**DELETE COMMAND**

CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Dave', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');



-- fetch 

-- SELECT \* FROM EMPLOYEE WHERE dept = 'Sales';

delete from EMPLOYEE where empId = 3;

SELECT \* FROM EMPLOYEE;

**Output:**



+-------+-------+------------+

| empId | name  | dept       |

+-------+-------+------------+

|     1 | Clark | Sales      |

|     2 | Dave  | Accounting |

+-------+-------+------------+





**DDL - Data Definition Language**

To chage the structure of data

1. Create

2\.     Alter - To Change in the existing table

3\.     Drop - Remove the database

4\.    Truncate - Remove the table



**DML - Data Manipulation Language**

1. Select

2\.      Update

3\.      Insert

4\.     Delete



**PRINT FIRST LETTER**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Aman', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');





SELECT \*  from EMPLOYEE where name like '%A';

**Output:**



+-------+------+-------+

| empId | name | dept  |

+-------+------+-------+

|     3 | Ava  | Sales |

+-------+------+-------+



**PRINT SECOND LETTER**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Aman', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');





SELECT \* from EMPLOYEE where name like '\_m%';

**Output:**



+-------+------+------------+

| empId | name | dept       |

+-------+------+------------+

|     2 | Aman | Accounting |

+-------+------+------------+



**ORDER BY NAME:(ASCENDING)**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Aman', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');





SELECT \* from EMPLOYEE order by name;

**Output:**



+-------+-------+------------+

| empId | name  | dept       |

+-------+-------+------------+

|     2 | Aman  | Accounting |

|     3 | Ava   | Sales      |

|     1 | Clark | Sales      |

+-------+-------+------------+





**ORDER BY NAME:(DESCENDING)**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Aman', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');





SELECT \* from EMPLOYEE order by name desc;

**Output:**



+-------+-------+------------+

| empId | name  | dept       |

+-------+-------+------------+

|     1 | Clark | Sales      |

|     3 | Ava   | Sales      |

|     2 | Aman  | Accounting |

+-------+-------+------------+



**SORTING :**



CREATE TABLE EMPLOYEE (

&nbsp; empId INTEGER PRIMARY KEY,

&nbsp; name TEXT NOT NULL,

&nbsp; dept TEXT NOT NULL

);



-- insert

INSERT INTO EMPLOYEE VALUES (0001, 'Clark', 'Sales');

INSERT INTO EMPLOYEE VALUES (0002, 'Aman', 'Accounting');

INSERT INTO EMPLOYEE VALUES (0003, 'Ava', 'Sales');







SELECT \* from EMPLOYEE limit 4;

SELECT count(\*), avg(empId), max(empId) from EMPLOYEE



**Output:**



+-------+-------+------------+

| empId | name  | dept       |

+-------+-------+------------+

|     1 | Clark | Sales      |

|     2 | Aman  | Accounting |

|     3 | Ava   | Sales      |

+-------+-------+------------+

+----------+------------+------------+

| count(\*) | avg(empId) | max(empId) |

+----------+------------+------------+

|        3 |     2.0000 |          3 |

+----------+------------+------------+







