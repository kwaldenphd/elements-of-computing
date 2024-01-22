# Subqueries & Wildcard Operators

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
