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

<h1>Sql Commands<h1>
<h2>ALTER TABLE:</h2>
<h3>ALTER TABLE lets you add columns to a table in a database.</h3>
<h4><code>ALTER TABLE table_name ADD column_name datatype;</code></h4>
<h2>AND</h2>
<h3>AND is an operator that combines two conditions. Both conditions must be true for the row
to be included in the result set.</h3>
<h4><code>SELECT column_name(s) FROM table_name WHERE column_1 = value_1 AND column_2 =
value_2;</code></h4>
<h4><code>Select gender from Person</code></h4>

<h2>AS</h2>
AS is a keyword in SQL that allows you to rename a column or table using an alias.
<h4><code>SELECT column_name AS 'Alias' FROM table_name;</h4></code>
<h2>AVG()</h2>
AVG() is an aggregate function that returns the average value for a numeric column.
SELECT AVG(column_name) FROM table_name;
<h2>BETWEEN</h2>
The BETWEEN operator is used to filter the result set within a certain range. The values
can be numbers, text or dates.
<h4><code>SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value_1 AND value_2;</h4></code>
<h2>CASE</h2>
CASE statements are used to create different outputs (usually in the SELECT statement). It
is SQL's way of handling if-then logic.
<h4><code>SELECT column_name,
CASE
WHEN condition1 THEN 'Result_1'
WHEN condition2 THEN 'Result_2'
ELSE 'Result_3'
END
FROM table_name;</h4></code>
<h2>COUNT()</h2>
COUNT() is a function that takes the name of a column as an argument and counts the
number of rows where the column is not NULL.
<h4><code>SELECT COUNT(column_name) FROM table_name;</h4></code>
<h2>CREATE TABLE</h2>
CREATE TABLE creates a new table in the database. It allows you to specify the name of
the table and the name of each column in the table.
<h4><code>CREATE TABLE table_name (
column_1 datatype,
column_2 datatype,
column_3 datatype
);</h4></code>
<h2>DELETE</h2>
 DELETE statements are used to remove rows from a table.
<h4><code>DELETE FROM table_name WHERE some_column = some_value;</h4></code>
<h2>GROUP BY</h2>
GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in
collaboration with the SELECT statement to arrange identical data into groups.
<h4><code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;</h4></code>
<h2>HAVING</h2>
HAVING was added to SQL because the WHERE keyword could not be used with
aggregate functions.
<h4><code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > value;</h4></code>
<h2>INNER JOIN</h2>
An inner join will combine rows from different tables if the join condition is true.
<h4><code>SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;</h4></code>
<h2>INSERT</h2>
INSERT statements are used to add a new row to a table.
<h4><code>INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2',
value_3);</h4></code>
<h2>IS NULL / IS NOT NULL</h2>
IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty
values.
<h4><code>SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;</h4></code>
<h2>LIKE</h2>
LIKE is a special operator used with the WHERE clause to search for a specific pattern in a
column.
<h4><code>SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;</h4></code>
<h2>LIMIT</h2>
LIMIT is a clause that lets you specify the maximum number of rows the result set will have.
<h4><code>SELECT column_name(s) FROM table_name LIMIT number;</h4></code>
<h2>MAX()</h2>
MAX() is a function that takes the name of a column as an argument and returns the largest
value in that column.
<h4><code>SELECT MAX(column_name) FROM table_name;</h4></code>
<h2>MIN()</h2>
MIN() is a function that takes the name of a column as an argument and returns the
smallest value in that column.
<h4><code>SELECT MIN(column_name) FROM table_name;</h4></code>
<h2>OR</h2>
OR is an operator that filters the result set to only include rows where either condition is
true.
<h4><code>SELECT column_name FROM table_name WHERE column_name = value_1 OR column_name =
value_2;</h4></code>
<h2>ORDER BY</h2>
ORDER BY is a clause that indicates you want to sort the result set by a particular column
either alphabetically or numerically.
<h4><code>SELECT column_name FROM table_name ORDER BY column_name ASC | DESC;</h4></code>
<h2>OUTER JOIN</h2>
An outer join will combine rows from different tables even if the join condition is not met.
Every row in the left table is returned in the result set, and if the join condition is not met,
then NULL values are used to fill in the columns from the right table.
<h3>LEFT OUTER JOIN</h3>
<h4><code>SELECT column_name(s) FROM table_1
LEFT JOIN table_2
ON table_1.column_name = table_2.column_name;</h4></code>
<h2>ROUND()</h2>
ROUND() is a function that takes a column name and an integer as an argument. It rounds
the values in the column to the number of decimal places specified by the integer.
<h4><code>SELECT ROUND(column_name, integer) FROM table_name;</h4></code>
<h2>SELECT</h2>
SELECT statements are used to fetch data from a database. Every query will begin with
SELECT.
<h4><code>SELECT column_name FROM table_name;</h4></code>
<h2>SELECT DISTINCT</h2>
SELECT DISTINCT specifies that the statement is going to be a query that returns unique
values in the specified column(s).
<h4><code>SELECT DISTINCT column_name FROM table_name;</h4></code>
<h2>SUM</h2>
SUM() is a function that takes the name of a column as an argument and returns the sum of
all the values in that column.
<h4><code>SELECT SUM(column_name) FROM table_name;</h4></code>
<h2>UPDATE</h2>
UPDATE statements allow you to edit rows in a table.
<h4><code>UPDATE table_name SET some_column = some_value WHERE some_column = some_value;</h4></code>
<h4><code>UPDATE movies SET movie_title = "NewMovieTitle" WHERE movie_year = "1977"</h4></code>
<h2>WHERE</h2>
WHERE is a clause that indicates you want to filter the result set to include only rows where
the following condition is true.
<h4><code>Select names from Person where gender = ‘Female’</h4></code>