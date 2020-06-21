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


### Basic data types in sql.

1. INT              Whole Numbers
2. DECIMAL(M,N)     Decimal Numbers - Exact value. 
- Example:DECIMAL(10,4) total 10 digits where 4 digits comes after decimal points
3. VARCHAR(l)       String of text of length l.
4. BLOB             Binary large Objects, Stores large data. --like images
5. DATE             'YYYY-MM-DD'
6. TIMESTAMP         'YYYY-MM-DD  HH:MM:SS' -used for recording


**-- Creating tables**
1. - CREATE TABLE student (
  - student_id INT PRIMARY KEY,
  - name VARCHAR(40),
  - major VARCHAR(40)
  - -- PRIMARY KEY(student_id)
);

2. **DESCRIBE student;**
3. **DROP TABLE student;**
4. **ALTER TABLE student ADD gpa DECIMAL;**
5. **ALTER TABLE student DROP COLUMN gpa;**
