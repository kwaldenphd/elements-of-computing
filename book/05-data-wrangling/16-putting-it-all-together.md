# Putting It All Together

This chapter covered a lot of ground. Let's review some of the core workflows we've encountered:

Interacting:
- Selecting
- Sorting
- Filtering
- Data types & time series data

Aggregating & calculating:
- Summary & descriptive statistics
- Arithmetic operations
- Split-apply-combine
  * `.groupby()` and `.value_counts()`

Reshaping:
- `.pivot` (long to wide)
- `.melt` (wide to long)
- `.pivot_table` (long to wide with summary statistic)
- `.transpose` (invert columns and rows)
- `.explode` (making multi-value columns distinct rows)

Combining:
- `.merge` (connects rows in DataFrames based on one or more key fields, similar to SQL JOIN operations)
- `.concat` (concatenates or "stacks" objects together along an axis)

## Resources

And we're just scratching the surface in terms of Pandas data reshaping operations.

A couple useful links:
- [Pandas documentation, reshaping data](https://pandas.pydata.org/docs/user_guide/reshaping.html)
- [Pandas documentation, merging & joining](https://pandas.pydata.org/docs/user_guide/merging.html)