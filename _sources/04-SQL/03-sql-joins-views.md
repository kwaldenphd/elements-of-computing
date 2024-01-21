# Joins & Views

SQL clauses are written in a fixed order:
<ol type="i">
<li><code>SELECT</code></li>
<li><code>FROM</code></li>
<li><code>WHERE</code></li>
<li><code>ORDER BY</code></li>
</ol>

But the order in which we write these clauses is not the order in which SQL executes them. SQL's order of execution:

Order | Clause | Function
--- | --- | ---
1 | `FROM` and `JOIN` | Choose and join tables to get base data
2 | `WHERE` | Filters the base data
3 | `GROUP BY` | Aggregates the base data
4 | `HAVING` | Filters the aggregated data
5 | `SELECT` | Returns the final data
6 | `ORDER BY` | Sorts the final data
7 | `LIMIT` | Limits the returned data based on row count

Why does order of execution matter? If we know the computational pipeline for how SQL executes a query, we can write more effecient and concise queries.

## Joins

The process of building a relational database in which you identify primary and foreign keys and build relationships across tables does not change the underlying data structure. We can accomplish this in SQL using `JOIN` functions.

According to W3Schools'[SQL Joins page](https://www.w3schools.com/sql/sql_join.asp), "A JOIN clause is used to combine rows from two or more tables, based on a related column between them."

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_3.jpg?raw=true" /></p>

Image credit: W3 Schools, ["Different Types of SQL Joins"](https://www.w3schools.com/sql/sql_join.asp) (n.d.)

There are four main types of `JOIN` functions.
- `(INNER) JOIN` returns matching records in both tables
- `LEFT (OUTER) JOIN` returns all records from the left table and only matching records from the right table
- `RIGHT (OUTER) JOIN` returns all records from the right table and only matching records from the left table
- `FULL (OUTER) JOIN` returns all matching records from both the left and right tables

We can express these `JOIN` functions programmatically in SQL.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_2.png?raw=true"/></p>

Image credit: C.L. Moffatt, ["Visual  Representations of SQL Joins"](https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins) *Code Project* (3 February 2009).

Sample syntax for these examples:

```SQL
-- left join example
SELECT [FIELD(S)]
FROM [TABLE 1]
LEFT JOIN [TABLE 2]
ON table1.field = table2.field;
```

```SQL
-- right join example
SELECT [FIELD(S)]
FROM [TABLE 1]
RIGHT JOIN [TABLE 2]
ON table1.field = table2.field;
```

```SQL
-- inner join example
SELECT [FIELD(S)]
FROM [TABLE 1]
INNER JOIN [TABLE 2]
ON table1.field = table2.field;
```

```SQL
-- full or outer join example
SELECT [FIELD(S)]
FROM [TABLE 1]
FULL OUTER JOIN [TABLE 2]
ON table1.field = table2.field;
```

Let's write a SQL statement that uses the `playerID` field to join the `transactions` and `players` tables.

```SQL
-- left join that joins matching records from players table
SELECT *
FROM transactions
LEFT JOIN players
ON transactions.playerID = players.playerID;
```

This query uses the `playerID` field and a left join to join the `transactions` and `players` tables. The query returns all columns in the left join query.

We could also write this query with the `USING` keyword.

```SQL
-- alternate syntax for left join that joins matching records from players table
SELECT *
FROM transactions
LEFT JOIN players
USING (playerID);
```
### Additional Resources

- W3Schools, ["SQL Joins"](https://www.w3schools.com/sql/sql_join.asp)
- SQL Joins Explained, ["Basic SQL Join Types"](http://www.sql-join.com/sql-join-types)
- ChartIO Data School, ["SQL Join Types Explained Visually"](https://dataschool.com/how-to-teach-people-sql/sql-join-types-explained-visually/)

## Saving Queries

Let's say you have a query or operation you perform frequently or on a regular basis. Having to remember and type out the full query syntax would be cumbersome. SQL gives you the option to save queries in the databases. These saved queries are called **Views**.

Let's say we wanted to create a view for a query that returns all data for teams in the Pacific Coast Leauge.

```SQL
-- syntax for saving a query
CREATE VIEW PCL AS
SELECT *
FROM teams
WHERE league="Pacific Coast League';
```

Now we have the `PCL` view we can access without having to type out the full query. To access the results using the newly-created view:

```SQL
-- syntax for accessing a saved query
SELECT * 
FROM PCL;
```

## Application

Q3: Write an SQL query that joins the Transactions and Team_Locations tables and returns all matching columns from the Transactions table. What kind of join is this? What data does this query return? Test your query using DB Browser. Include code + comments.

Q4: Write an SQL query to return the data from the `players` table, sorted in chronological order by birth year and reverse alphabetical order by country. Test your query using DB Browser. Include code + comments.

Q5: Write an SQL query to return all data from the `players` table for players born in cities that start with the letter “S”. Test your query using DB Browser. Include code + comments.