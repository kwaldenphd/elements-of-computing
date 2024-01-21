# Basic Syntax

What is SQL? As described in Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html), "Structured Query Language, or SQL (sometimes pronounced 'sequel'), is a powerful language used to interrogate and manipulate relational databases. It is not a general programming language that you can use to write an entire program."

When working with relational database systems, we can use SQL to write queries. As described in Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html), "a query is a question or request for data. For example, “How many journals does our library subscribe to?” When we query a database, we can ask the same question using a common language called Structured Query Language or SQL in what is called a statement. Some of the most useful queries - the ones we are introducing in this first section - are used to return results from a table that match specific criteria."

## DB Browser Setup

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_4.jpg?raw=true" /></p>

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_5.jpg?raw=true" /></p>

In the DB Browser program, select the `Open Database` icon. Open the `.db` file from the previous section.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_6.jpg?raw=true" /></p>

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_7.jpg?raw=true" /></p>

Click the `Execute SQL` tab. The top text-box on the left-hand pane in the program (immediately below `SQL 1`) is where we will type SQL statements.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_8.jpg?raw=true" /></p>

Once we start adding SQL syntax, we can run all (or a selection) using the single arrow icon (left of the two arrows, immediate right of print). 
- We can use the other arrow (right of the two arrows) to run a single line.

## Comments

We can add single-line comments to our SQL statements using a double dash `--`.

```SQL
-- this is my single-line comment
```

## Selecting

The `SELECT` query selects a specific field (column) from a specific table. The semicolon `;` is required at the end of every SQL query.

```SQL
-- sample syntax for select
SELECT [field]
FROM [table];
```

Adding multiple columns after `SELECT` will return data from multiple columns.

```SQL
-- sample syntax for selecting multiple fields
SELECT [field_1], [field_2], [field_3]
FROM [table];
```

### `SELECT DISTINCT`

We might want to write a query to return all the unique values in a particular field. For example, selecting the entire `country` field in the `Player_Birthplaces` table would return many duplicate values.

```SQL
-- sample syntax for selecting unique values
SELECT DISTINCT [field]
FROM [table];
```

`SELECT DISTINCT` returns a list of unique values.

## Sorting

We might also want to sort the results returned by a query.

```SQL
-- sample syntax that selects all values from a table and orders by specific file
SELECT *
FROM [table]
ORDER BY [field] ASC;
```

The `*` wildcard operator selects all the fields in a specific table. `ORDER BY` specifies a field to use in sorting the query results. `ASC` returns ascending results. `DESC` would return descending results.

We can also sort on multiple fields.

```SQL
-- sample syntax that selects all values from a table and orders by two fields
SELECT *
FROM [table]
ORDER BY [field_1] ASC, [field_2] DESC;
```

In the query above, the `ORDER BY` statement sorts `[field_1]` first (ascending) and then sorts `[field_2]` (descending).

## Filtering

Sometimes we may only want to return values that fall within a specific range or based on a particular set of conditions.

```SQL
-- select all values where country = "DO"
SELECT *
FROM locations
WHERE country='DO';
```

This query returns all columns from the `locations` table where data in the `country` field is equal to `DO`. The data returned by this query includes all the records for locations in the Dominican Republic.

Other comparison operators in SQL include:

Operator | Description
--- | ---
`=` | Equal to
`>` | Greater than
`<` | Less than
`>=` | Greater than or equal to
`<=` | less than or equal to
`<>` | Not equal to
`BETWEEN` | Between a specified range
`LIKE` | Searches for a pattern based on similarity
`IN` | Specifies multiple possible values for a column

### `WHERE`

For more on operators  that can be used in a `WHERE` clause (from W3Schools [SQL Where Clause page](https://www.w3schools.com/sql/sql_where.asp)).

We can also use operators to specify a range for the `WHERE` clause.

```SQL
-- select values where dob is greater than 1996
SELECT *
FROM players
WHERE dob>1996;
```

This query returns all columns from `players` where data in the `dob` field is greater than `1996`. SQL query syntax requires single quotes around text values. Numeric fields do not need single quotes.

## Subqueries

We can also write queries that test for or return values for multiple conditions, using SQL's logical operators. These are called **subqueries**. For example, what if we wanted to return all records for locations in the Dominican Republic, Venezuela, or Puerto Rico.

```SQL
-- select all values from table where country equals any of three values
SELECT *
FROM locations
WHERE (country = 'DO') OR (country = 'VE') OR (country = 'PR');
```

Other SQL operators include:

Operator | Description
--- | ---
`ALL` | TRUE if all subquery values meet the condition
`AND` | TRUE if all the conditions separated by AND is TRUE
`ANY` | TRUE if any of the subquery values meet the condition
`BETWEEN` | TRUE if the operand is within the range of comparisons
`EXISTS` | TRUE if the subquery returns one or more records
`IN` | True if the operand is equal to one of a list of expressions
`LIKE` |  TRUE if the operand matches a pattern
`NOT` | Displays a record if the condition(s) is NOT TRUE
`OR` | TRUE if any of the conditions separated by OR is TRUE
`SOME` | TRUE if any of the subquery values meet the condition

<blockquote>Learn more about operators at Beginner SQL's <a href="https://beginner-sql-tutorial.com/sql-like-in-operators.htm">Tutorial on SQL Comparison Keywords</a>.</blockquote>

## Wildcard Operators

SQL has a number of wildcard operators that (like regular expressions, or regex commands) can be useful to substitute one or more characters in a string.

Symbol | Description | Example
--- | --- |---
`%` | Represents zero or more characters | `bl%` returns bl, black, blue, and blob
`_` | Represents a single character | `h_t` returns hot, hat, and hit
`[]` | Represents any single character within the brackets | `h[oa]t` returns hot and hat, but not hit
`^` | Represents any character not in the brackets | `h[^oa]t` returns hit, but not hot and hat
`-` | Represents a range of characters | `c[a-b]t` finds cat and cbt

When using wildcard characters to search or match a string, we use the `LIKE` operator in combination with the `WHERE` clause.

For example:
```SQL
-- sample syntax for WHERE and LIKE
SELECT *
FROM TABLE
WHERE FIELD LIKE 'WILDCARD EXPRESSION';
```

<blockquote>Check out W3Schools <a href="https://www.w3schools.com/sql/sql_wildcards.asp">"SQL Wildcards"</a> for more on wildcard characters in SQL.</blockquote>

We can use `WHERE` and `LIKE` in combination with wildcard operators to filter records based on string character patterns.

## Aggregating and Calculating

SQL contains functions which allow you to make calculations on data in your database for reports. 

Some of the most common functions include:
- `MAX`: returns the maximum value in a field
- `MIN`: returns the minimum value in a field
- `AVG`: returns the average value of a field
- `COUNT`: counts the number of values in a field and returns the total
- `SUM`: adds the values in a field and returns the sum

Let's say we wanted to get the average birth year for players in our dataset. We can use `AVG` in our query.

```SQL
-- get average DoB from specific table
SELECT AVG(DoB)
FROM players;
```

We can filter the results of aggregate functions using the `HAVING` keyword.
  * NOTE: The `HAVING` keyword has to be used in combination with `GROUP BY`.

Let's say we only wanted to see the average birth year for players born after 1990.

```SQL
-- get average DoB from specific table only for records that meet a specific condition
SELECT AVG(DoB)
FROM players
GROUP BY LocationID
HAVING DoB > 1990;
```

<blockquote>Check out W3Schools <a href="https://www.w3schools.com/sql/sql_operators.asp">"SQL Operators"</a> page to learn more about SQL Operators, including arithmetic, comparison, compound, and logical operators.</blockquote>

In SQL, we can also perform calculations as part of a query. We can use expressions on a column or multiple columns to get new values during our query. The results of these calculations are known as **computed columns**.

SQL's arithmetic operators include:

Operator | Description
--- | ---
`+` | Add
`-` | Subtract
`*` | Multiply
`/` | Divide
`%` | Modulo

For example, let's say we had temperature data in Fahrenheit and needed those values in Celsius, rounded to two decimal places. We could make this conversion using SQL's arithmetic operators.

```SQL
-- sample syntax for temperature conversion formula
SELECT temp, round(5 * (temp_reading - 32) / 9, 2) as Celsius FROM Temp_Data WHERE quant = 'temp';
```

### Additional Resources

- Library Carpentry's SQL tutorial, ["Aggregating & Calculating Values"](https://librarycarpentry.org/lc-sql/04-aggregating-calculating/index.html) 
- Software Carpentry's Databases and SQL tutorial, ["Calculating New Values"](https://swcarpentry.github.io/sql-novice-survey/)
- W3Schools' [SQL Tutorial](https://www.w3schools.com/sql/default.asp) pages for specific aggregating and calculating functions.

## Application

Q1: Write a query that gets average birth year from the `players` table, for players born after 1985. Test your query using DB Browser. Include code + comments.

Q2: Write a SQL query that returns a unique list of team names from the `teams` table, sorted in reverse alphabetical order. Test your query using DB Browser. Include code + comments.