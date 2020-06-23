# Core-Cs
## DBMS | OS | OOPs from basic to advance.



### DBMS

* To start MySql Server run this command in your command prompt (Path of the file may be different I am doing this for general case);

1. C:\>cd xampp
  - C:\xampp>cd MySQL 
    - C:\xampp\mysql>cd bin 
     - C:\xampp\mysql\bin>mysql -h localhost -u root
* Hit ENTER if the password is an empty string. Now you are in. You can list all available databases, and select one using the fallowing:

* SHOW DATABASES;


## Basic data types in sql.

1. INT              Whole Numbers
2. DECIMAL(M,N)     Decimal Numbers - Exact value. 
- Example:DECIMAL(10,4) total 10 digits where 4 digits comes after decimal points
3. VARCHAR(l)       String of text of length l.
4. BLOB             Binary large Objects, Stores large data. --like images
5. DATE             'YYYY-MM-DD'
6. TIMESTAMP         'YYYY-MM-DD  HH:MM:SS' -used for recording


## -- Creating tables
1.   CREATE TABLE student (  <br/>
     student_id INT PRIMARY KEY, <br/>
     name VARCHAR(40),<br/>
     major VARCHAR(40)<br/>
     -- PRIMARY KEY(student_id)<br/>

);

### output:
+--------+-------------+------+-----+---------+-------+<br/>
| Field  | Type        | Null | Key | Default | Extra |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
| stu_id | int(11)     | NO   | PRI | NULL    |       |<br/>
| name   | varchar(40) | YES  |     | NULL    |       |<br/>
| major  | varchar(40) | YES  |     | NULL    |       |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
1. **DESCRIBE student;** --TO describe Table of student or desc structure of the table.
2. **DROP TABLE student;** --remove table from database(warn)
3. **ALTER TABLE student ADD gpa DECIMAL;** --add column gpa
4. **ALTER TABLE student DROP COLUMN gpa;**  --remove column gpa

## INSERT 
1. **INSERT INTO student VALUES(1,"RAKESH",'CSE');**<br/>
Query OK, 1 row affected (0.207 sec)<br/>

2. **MariaDB [db]> DESC student;**<br/>
+--------+-------------+------+-----+---------+-------+<br/>
| Field  | Type        | Null | Key | Default | Extra |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
| stu_id | int(11)     | NO   | PRI | NULL    |       |<br/>
| name   | varchar(40) | YES  |     | NULL    |       |<br/>
| major  | varchar(40) | YES  |     | NULL    |       |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
3 rows in set (0.329 sec)<br/>

3. **SELECT * FROM student;** --TO Show table<br/>
+--------+--------+-------+<br/>
| stu_id | name   | major |<br/>
+--------+--------+-------+<br/>
|      1 | RAKESH | CSE   |<br/>
+--------+--------+-------+<br/>
1 row in set (0.071 sec)<br/>

4. **INSERT INTO student(stu_id,name) values(2,"SANTOSH");**<br/>
Query OK, 1 row affected (0.135 sec)<br/>

5. SELECT * FROM student;<br/>
+--------+---------+-------+<br/>
| stu_id | name    | major |<br/>
+--------+---------+-------+<br/>
|      1 | RAKESH  | CSE   |<br/>
|      2 | SANTOSH | NULL  |<br/>
+--------+---------+-------+<br/>
2 rows in set (0.000 sec)<br/>
## CONSTRAINTS
1. **CREATE TABLE student**(<br/>
     stu_id INT PRIMARY KEY,<br/>
     name VARCHAR(40) UNIQUE,<br/>
     major VARCHAR(40) NOT NULL,<br/>
     );<br/>
Query OK, 0 rows affected (0.579 sec)<br/>

2. **MariaDB [db]> DESC student;**<br/>
+--------+-------------+------+-----+---------+-------+<br/>
| Field  | Type        | Null | Key | Default | Extra |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
| stu_id | int(11)     | NO   | PRI | NULL    |       |<br/>
| name   | varchar(40) | YES  | UNI | NULL    |       |<br/>
| major  | varchar(40) | NO   |     | NULL    |       |<br/>
+--------+-------------+------+-----+---------+-------+<br/>
3 rows in set (0.355 sec)<br/>

3. **MariaDB [db]> INSERT INTO student values(1,"Amrit","CSE");** <br/>
Query OK, 1 row affected (0.310 sec)<br/>

4. **MariaDB [db]> INSERT INTO student values(1,"Amrit","BIOLOGY");**<br/>
ERROR 1062 (23000): Duplicate entry '1' for key 'PRIMARY'<br/>
5. **MariaDB [db]> INSERT INTO student values(4,"Amrit",NULL);**<br/>
ERROR 1048 (23000): Column 'major' cannot be null<br/>
6. **MariaDB [db]> ALTER TABLE student add Payment INT DEFAULT 0;**<br/>
Query OK, 0 rows affected (0.337 sec)<br/>
Records: 0  Duplicates: 0  Warnings: 0<br/>

7.**MariaDB [db]> DESC student;**<br/>
+---------+-------------+------+-----+---------+-------+<br/>
| Field   | Type        | Null | Key | Default | Extra |<br/>
+---------+-------------+------+-----+---------+-------+<br/>
| stu_id  | int(11)     | NO   | PRI | NULL    |       |<br/>
| name    | varchar(40) | YES  | UNI | NULL    |       |<br/>
| major   | varchar(40) | NO   |     | NULL    |       |<br/>
| Payment | int(11)     | YES  |     | 0       |       |<br/>
+---------+-------------+------+-----+---------+-------+<br/>
4 rows in set (0.033 sec)<br/>
**NOTE**
1. Primary key will not accept NULL values whereas Unique key can accept one NULL value.<br/>
2. A table can have only primary key whereas there can be multiple unique key on a table.<br/>
3. A Clustered index automatically created when a primary key is defined whereas Unique key generates the non-clustered index.<br/>
