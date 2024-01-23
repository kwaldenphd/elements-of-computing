# Filters & Conditions

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