# Core-Cs
**DBMS | OS | OOP**
<h3><code>Welcome to Core-Cs</code></h3>
<blockquote><strong>Do you have less time for your interview preperation then you are at the right place. please follow this article  and finally  you will find that in less time you have covered almost all the  important topics related to core-cs.</strong></blockquote>

<blockquote>
<a href = "mailto: rrlinus5@gmail.com">rrlinus5@gmail.com</a></br>
<a href = "tel:+919304180922">Call me at +919304180922</a></br>
<a href = "https://www.linkedin.com/in/rakesh-raj-15a64916b/">Linkedin</a></br>
</blockquote>

<strong><i>Note:currently-- I am working on this repo.</i></strong>

<h2> DBMS</h2>

<p><i>To start MySql Server run this command in your command prompt (Path of the file may be different I am doing this for general case);<i></p>

 - <code>C:\>cd xampp</code>
  - <code>C:\xampp>cd MySQL </code>
    - <code>C:\xampp\mysql>cd bin </code>
     - <code>C:\xampp\mysql\bin>mysql -h localhost -u root</code>
<p><i> Hit ENTER if the password is an empty string. Now you are in. You can list all available databases, and select one using the fallowing:</><i></p>

<code> SHOW DATABASES;</code></>


<h3>Basic data types in sql.</h3>
<ul>
<li> <code>INT</code>              Whole Numbers</></li>
<li><code> DECIMAL(M,N)</code>      Decimal Numbers - Exact value. </></li>
 <h5>Example:DECIMAL(10,4) total 10 digits where 4 digits comes after decimal points</h5>
<li><code> VARCHAR(l)</code>        String of text of length l.</></li>
<li><code> BLOB      </code>        Binary large Objects, Stores large data. --like images</></li>
<li><code> DATE    </code>          'YYYY-MM-DD'</></li>
<li><code>TIMESTAMP </code>         'YYYY-MM-DD  HH:MM:SS' -used for recording</></li>
</ul>
<h1>Sql Commands<h1>
<h3>ALTER TABLE:</h3>
<p><i>ALTER TABLE lets you add columns to a table in a database.<i></p>
<code>ALTER TABLE table_name ADD column_name datatype;</code></>
<h3>AND</h3>
<p><i>AND is an operator that combines two conditions. Both conditions must be true for the row
to be included in the result set.><i></p>
<code>SELECT column_name(s) FROM table_name WHERE column_1 = value_1 AND column_2 =
value_2;</code></>
<code>Select gender from Person</code></>

<h3>AS</h3>
<p><i>AS is a keyword in SQL that allows you to rename a column or table using an alias.<i></p>
<code>SELECT column_name AS 'Alias' FROM table_name;</></code>
<h3>AVG()</h3>
<p><i>AVG() is an aggregate function that returns the average value for a numeric column.<i></p>
<code>SELECT AVG(column_name) FROM table_name;</></code>
<h3>BETWEEN</h3>
<p><i>The BETWEEN operator is used to filter the result set within a certain range. The values
can be numbers, text or dates.<i></p>
<code>SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value_1 AND value_2;</></code>
<h3>CASE</h3>
<p><i>CASE statements are used to create different outputs (usually in the SELECT statement). It
is SQL's way of handling if-then logic.<i></p>
<code>SELECT column_name,
CASE
WHEN condition1 THEN 'Result_1'
WHEN condition2 THEN 'Result_2'
ELSE 'Result_3'
END
FROM table_name;</></code>
<h3>COUNT()</h3>
<p><i>COUNT() is a function that takes the name of a column as an argument and counts the
number of rows where the column is not NULL.<i></p>
<code>SELECT COUNT(column_name) FROM table_name;</></code>
<h3>CREATE TABLE</h3>
<p><i>CREATE TABLE creates a new table in the database. It allows you to specify the name of
the table and the name of each column in the table.<i></p>
<code>CREATE TABLE table_name (
column_1 datatype,
column_2 datatype,
column_3 datatype
);</></code>
<h3>DELETE</h3>
 <p><i>DELETE statements are used to remove rows from a table.<i></p>
<code>DELETE FROM table_name WHERE some_column = some_value;</></code>
<h3>GROUP BY</h3>
<p><i>GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in
collaboration with the SELECT statement to arrange identical data into groups.<i></p>
<code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;</></code>
<h3>HAVING</h3>
<p><i>HAVING was added to SQL because the WHERE keyword could not be used with
aggregate functions.<i></p>
<code>SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > value;</></code>
<h3>INNER JOIN</h3>
<p><i>An inner join will combine rows from different tables if the join condition is true.<i></p>
<code>SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;</></code>
<h3>INSERT</h3>
<p><i>INSERT statements are used to add a new row to a table.<i></p>
<code>INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2',
value_3);</></code>
<h3>IS NULL / IS NOT NULL</h3>
<p><i>IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty
values.<i></p>
<code>SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;</></code>
<h3>LIKE</h3>
<p><i>LIKE is a special operator used with the WHERE clause to search for a specific pattern in a
column.<i></p>
<code>SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;</></code>
<h3>LIMIT</h3>
<p><i>LIMIT is a clause that lets you specify the maximum number of rows the result set will have.<i></p>
<code>SELECT column_name(s) FROM table_name LIMIT number;</></code>
<h3>MAX()</h3>
<p><i>MAX() is a function that takes the name of a column as an argument and returns the largest
value in that column.<i></p>
<code>SELECT MAX(column_name) FROM table_name;</></code>
<h3>MIN()</h3>
<p><i>MIN() is a function that takes the name of a column as an argument and returns the
smallest value in that column.<i></p>
<code>SELECT MIN(column_name) FROM table_name;</></code>
<h3>OR</h3>
<p><i>OR is an operator that filters the result set to only include rows where either condition is
true.<i></p>
<code>SELECT column_name FROM table_name WHERE column_name = value_1 OR column_name =
value_2;</></code>
<h3>ORDER BY</h3>
<p><i>ORDER BY is a clause that indicates you want to sort the result set by a particular column
either alphabetically or numerically.<i></p>
<code>SELECT column_name FROM table_name ORDER BY column_name ASC | DESC;</></code>
<h3>OUTER JOIN</h3>
<p><i>An outer join will combine rows from different tables even if the join condition is not met.<i></p>
<p><i>Every row in the left table is returned in the result set, and if the join condition is not met,
then NULL values are used to fill in the columns from the right table.<i></p>
<h5>LEFT OUTER JOIN</h5>
<code>SELECT column_name(s) FROM table_1
LEFT JOIN table_2
ON table_1.column_name = table_2.column_name;</></code>
<h3>ROUND()</h3>
<p><i>ROUND() is a function that takes a column name and an integer as an argument. It rounds
the values in the column to the number of decimal places specified by the integer.<i></p>
<code>SELECT ROUND(column_name, integer) FROM table_name;</></code>
<h3>SELECT</h3>
<p><i>SELECT statements are used to fetch data from a database. Every query will begin with
SELECT.<i></p>
<code>SELECT column_name FROM table_name;</></code>
<h3>SELECT DISTINCT</h3>
<p><i>SELECT DISTINCT specifies that the statement is going to be a query that returns unique
values in the specified column(s).<i></p>
<code>SELECT DISTINCT column_name FROM table_name;</></code>
<h3>SUM</h3>
<p><i>SUM() is a function that takes the name of a column as an argument and returns the sum of
all the values in that column.<i></p>
<code>SELECT SUM(column_name) FROM table_name;</></code>
<h3>UPDATE</h3>
<p><i>UPDATE statements allow you to edit rows in a table.<i></p>
<code>UPDATE table_name SET some_column = some_value WHERE some_column = some_value;</></code>
<code>UPDATE movies SET movie_title = "NewMovieTitle" WHERE movie_year = "1977"</></code>
<h3>WHERE</h3>
<p><i>WHERE is a clause that indicates you want to filter the result set to include only rows where
the following condition is true.<p><i>
<code>Select names from Person where gender = ‘Female’</></code>