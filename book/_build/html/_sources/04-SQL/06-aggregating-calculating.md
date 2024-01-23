# Aggregating and Calculating

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

## Additional Resources

- Library Carpentry's SQL tutorial, ["Aggregating & Calculating Values"](https://librarycarpentry.org/lc-sql/04-aggregating-calculating/index.html) 
- Software Carpentry's Databases and SQL tutorial, ["Calculating New Values"](https://swcarpentry.github.io/sql-novice-survey/)
- W3Schools' [SQL Tutorial](https://www.w3schools.com/sql/default.asp) pages for specific aggregating and calculating functions.