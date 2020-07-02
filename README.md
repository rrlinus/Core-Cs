# Core-Cs
## DBMS | OS | OOPs from basic to advance.



<h2> DBMS</h2>

<i>To start MySql Server run this command in your command prompt (Path of the file may be different I am doing this for general case);</i></h4>

 - <code>C:\>cd xampp</code>
  - <code>C:\xampp>cd MySQL </code>
    - <code>C:\xampp\mysql>cd bin </code>
     - <code>C:\xampp\mysql\bin>mysql -h localhost -u root</code>
<i> Hit ENTER if the password is an empty string. Now you are in. You can list all available databases, and select one using the fallowing:</></i>

<code> SHOW DATABASES;</code></>


<h3>Basic data types in sql.</h3>
<ul>
<li> INT              Whole Numbers</></li>
<li> DECIMAL(M,N)     Decimal Numbers - Exact value. </></li>
- Example:DECIMAL(10,4) total 10 digits where 4 digits comes after decimal points</></li>
<li> VARCHAR(l)       String of text of length l.</></li>
<li> BLOB             Binary large Objects, Stores large data. --like images</></li>
<li> DATE             'YYYY-MM-DD'</></li>
<li>TIMESTAMP         'YYYY-MM-DD  HH:MM:SS' -used for recording</></li>
</ul>
<h1>Sql Commands<h1>
<h3>ALTER TABLE:</h3>
<i>ALTER TABLE lets you add columns to a table in a database.</i></h4>
<code>ALTER TABLE table_name ADD column_name datatype;</code></>
<h3>AND</h3>
<i>AND is an operator that combines two conditions. Both conditions must be true for the row
to be included in the result set.></i></h4>
<code>SELECT column_name(s) FROM table_name WHERE column_1 = value_1 AND column_2 =
value_2;</code></>
<code>Select gender from Person</code></>

<h3>AS</h3>
<i>AS is a keyword in SQL that allows you to rename a column or table using an alias.</i></h4>
<code>SELECT column_name AS 'Alias' FROM table_name;</></code>
<h3>AVG()</h3>
<i>AVG() is an aggregate function that returns the average value for a numeric column.</i></h4>
<code>SELECT AVG(column_name) FROM table_name;</></code>
<h3>BETWEEN</h3>
<i>The BETWEEN operator is used to filter the result set within a certain range. The values
can be numbers, text or dates.</i></h4>
<code>SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value_1 AND value_2;</></code>
<h3>CASE</h3>
<i>CASE statements are used to create different outputs (usually in the SELECT statement). It
is SQL's way of handling if-then logic.</i></h4>
<code>SELECT column_name,
CASE
WHEN condition1 THEN 'Result_1'
WHEN condition2 THEN 'Result_2'
ELSE 'Result_3'
END
FROM table_name;</></code>
<h3>COUNT()</h3>
<i>COUNT() is a function that takes the name of a column as an argument and counts the
number of rows where the column is not NULL.</i></h4>
<code>SELECT COUNT(column_name) FROM table_name;</></code>
<h3>CREATE TABLE</h3>
<i>CREATE TABLE creates a new table in the database. It allows you to specify the name of
the table and the name of each column in the table.</i></h4>
<code>CREATE TABLE table_name (
column_1 datatype,
column_2 datatype,
column_3 datatype
);</></code>
<h3>DELETE</h3>
 <i>DELETE statements are used to remove rows from a table.</i></h4>
<code>DELETE FROM table_name WHERE some_column = some_value;</></code>
<h3>GROUP BY</h3>
<i>GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in
collaboration with the SELECT statement to arrange identical data into groups.</i></h4>
<code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;</></code>
<h3>HAVING</h3>
<i>HAVING was added to SQL because the WHERE keyword could not be used with
aggregate functions.</i></h4>
<code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > value;</></code>
<h3>INNER JOIN</h3>
<i>An inner join will combine rows from different tables if the join condition is true.</i></h4>
<code>SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;</></code>
<h3>INSERT</h3>
<i>INSERT statements are used to add a new row to a table.</i></h4>
<code>INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2',
value_3);</></code>
<h3>IS NULL / IS NOT NULL</h3>
<i>IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty
values.</i></h4>
<code>SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;</></code>
<h3>LIKE</h3>
<i>LIKE is a special operator used with the WHERE clause to search for a specific pattern in a
column.</i></h4>
<code>SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;</></code>
<h3>LIMIT</h3>
<i>LIMIT is a clause that lets you specify the maximum number of rows the result set will have.</i></h4>
<code>SELECT column_name(s) FROM table_name LIMIT number;</></code>
<h3>MAX()</h3>
<i>MAX() is a function that takes the name of a column as an argument and returns the largest
value in that column.</i></h4>
<code>SELECT MAX(column_name) FROM table_name;</></code>
<h3>MIN()</h3>
<i>MIN() is a function that takes the name of a column as an argument and returns the
smallest value in that column.</i></h4>
<code>SELECT MIN(column_name) FROM table_name;</></code>
<h3>OR</h3>
<i>OR is an operator that filters the result set to only include rows where either condition is
true.</i></h4>
<code>SELECT column_name FROM table_name WHERE column_name = value_1 OR column_name =
value_2;</></code>
<h3>ORDER BY</h3>
<i>ORDER BY is a clause that indicates you want to sort the result set by a particular column
either alphabetically or numerically.</i></h4>
<code>SELECT column_name FROM table_name ORDER BY column_name ASC | DESC;</></code>
<h3>OUTER JOIN</h3>
<code>An outer join will combine rows from different tables even if the join condition is not met.
<i>Every row in the left table is returned in the result set, and if the join condition is not met,
then NULL values are used to fill in the columns from the right table.</i></h4>
LEFT OUTER JOIN</h4>
<code>SELECT column_name(s) FROM table_1
LEFT JOIN table_2
ON table_1.column_name = table_2.column_name;</></code>
<h3>ROUND()</h3>
<i>ROUND() is a function that takes a column name and an integer as an argument. It rounds
the values in the column to the number of decimal places specified by the integer.</i></h4>
<code>SELECT ROUND(column_name, integer) FROM table_name;</></code>
<h3>SELECT</h3>
<i>SELECT statements are used to fetch data from a database. Every query will begin with
SELECT.</i></h4>
<code>SELECT column_name FROM table_name;</></code>
<h3>SELECT DISTINCT</h3>
<i>SELECT DISTINCT specifies that the statement is going to be a query that returns unique
values in the specified column(s).</i></h4>
<code>SELECT DISTINCT column_name FROM table_name;</></code>
<h3>SUM</h3>
<i>SUM() is a function that takes the name of a column as an argument and returns the sum of
all the values in that column.</i></h4>
<code>SELECT SUM(column_name) FROM table_name;</></code>
<h3>UPDATE</h3>
<i>UPDATE statements allow you to edit rows in a table.</i></h4>
<code>UPDATE table_name SET some_column = some_value WHERE some_column = some_value;</></code>
<code>UPDATE movies SET movie_title = "NewMovieTitle" WHERE movie_year = "1977"</></code>
<h3>WHERE</h3>
<i>WHERE is a clause that indicates you want to filter the result set to include only rows where
the following condition is true.<i></h4>
<code>Select names from Person where gender = ‘Female’</></code>