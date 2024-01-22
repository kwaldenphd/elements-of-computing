# Select & Sort

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