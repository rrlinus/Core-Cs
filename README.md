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

## Sql Commands
**ALTER TABLE:**
ALTER TABLE lets you add columns to a table in a database.
ALTER TABLE table_name ADD column_name datatype;
**AND**
<p>AND is an operator that combines two conditions. Both conditions must be true for the row
to be included in the result set.<p>
<p>SELECT column_name(s) FROM table_name WHERE column_1 = value_1 AND column_2 =
value_2;</p>
<p>Select gender from Person</p>

 **AS**
 <p>AS is a keyword in SQL that allows you to rename a column or table using an alias.
SELECT column_name AS 'Alias' FROM table_name;<p>
AVG()
AVG() is an aggregate function that returns the average value for a numeric column.
SELECT AVG(column_name) FROM table_name;
BETWEEN
The BETWEEN operator is used to filter the result set within a certain range. The values
can be numbers, text or dates.
SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value_1 AND value_2;
CASE
CASE statements are used to create different outputs (usually in the SELECT statement). It
is SQL's way of handling if-then logic.
SELECT column_name,
CASE
WHEN condition1 THEN 'Result_1'
WHEN condition2 THEN 'Result_2'
ELSE 'Result_3'
END
FROM table_name;
COUNT()
COUNT() is a function that takes the name of a column as an argument and counts the
number of rows where the column is not NULL.
SELECT COUNT(column_name) FROM table_name;
CREATE TABLE
CREATE TABLE creates a new table in the database. It allows you to specify the name of
the table and the name of each column in the table.
CREATE TABLE table_name (
column_1 datatype,
column_2 datatype,
column_3 datatype
);
DELETE
DELETE statements are used to remove rows from a table.
DELETE FROM table_name WHERE some_column = some_value;
GROUP BY
GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in
collaboration with the SELECT statement to arrange identical data into groups.
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;
HAVING
HAVING was added to SQL because the WHERE keyword could not be used with
aggregate functions.
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > value;
INNER JOIN
An inner join will combine rows from different tables if the join condition is true.
SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;
INSERT
INSERT statements are used to add a new row to a table.
INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2',
value_3);
IS NULL / IS NOT NULL
IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty
values.
SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;
LIKE
LIKE is a special operator used with the WHERE clause to search for a specific pattern in a
column.
SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;
LIMIT
LIMIT is a clause that lets you specify the maximum number of rows the result set will have.
SELECT column_name(s) FROM table_name LIMIT number;
MAX()
MAX() is a function that takes the name of a column as an argument and returns the largest
value in that column.
SELECT MAX(column_name) FROM table_name;
MIN()
MIN() is a function that takes the name of a column as an argument and returns the
smallest value in that column.
SELECT MIN(column_name) FROM table_name;
OR
OR is an operator that filters the result set to only include rows where either condition is
true.
SELECT column_name FROM table_name WHERE column_name = value_1 OR column_name =
value_2;
ORDER BY
ORDER BY is a clause that indicates you want to sort the result set by a particular column
either alphabetically or numerically.
SELECT column_name FROM table_name ORDER BY column_name ASC | DESC;
OUTER JOIN
An outer join will combine rows from different tables even if the join condition is not met.
Every row in the left table is returned in the result set, and if the join condition is not met,
then NULL values are used to fill in the columns from the right table.
LEFT OUTER JOIN
SELECT column_name(s) FROM table_1
LEFT JOIN table_2
ON table_1.column_name = table_2.column_name;
ROUND()
ROUND() is a function that takes a column name and an integer as an argument. It rounds
the values in the column to the number of decimal places specified by the integer.
SELECT ROUND(column_name, integer) FROM table_name;
SELECT
SELECT statements are used to fetch data from a database. Every query will begin with
SELECT.
SELECT column_name FROM table_name;
SELECT DISTINCT
SELECT DISTINCT specifies that the statement is going to be a query that returns unique
values in the specified column(s).
SELECT DISTINCT column_name FROM table_name;
SUM
SUM() is a function that takes the name of a column as an argument and returns the sum of
all the values in that column.
SELECT SUM(column_name) FROM table_name;
UPDATE
UPDATE statements allow you to edit rows in a table.
UPDATE table_name SET some_column = some_value WHERE some_column = some_value;
UPDATE movies SET movie_title = "NewMovieTitle" WHERE movie_year = "1977"
WHERE
WHERE is a clause that indicates you want to filter the result set to include only rows where
the following condition is true.
Select names from Person where gender = ‘Female’