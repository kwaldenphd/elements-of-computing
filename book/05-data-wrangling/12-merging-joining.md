# Merging & Joining

The SQL queries and joins lab covered how we can use joins in a relational database system to create new data structures. `pandas` has somewhat similar functionality that allows you to merge and combine data from multiple tables.

As with the reshaping functions, `Pandas` includes functionality geared toward combining or connecting different datasets.

A digest of these operations, courtesty of [Pandas documentation](https://pandas.pydata.org/docs/user_guide/merging.html):

* `pandas.concat`: Merge multiple `Series` or `DataFrame` objects along a shared index or column
* `DataFrame.join`: Merge multiple `DataFrame` objects along the columns
* `DataFrame.combine_first`: Update missing values with non-missing values in the same location
* `pandas.merge`: Combine two `Series` or `DataFrame` objects with SQL-style joining
  * `pandas.merge_ordered`: Combine two `Series` or `DataFrame` objects along an ordered axis
  * `pandas.merge_asof`: Combine two `Series` or `DataFrame` objects by near instead of exact matching keys
* `Series.compare` and `DataFrame.compare`: Show differences in values between two `Series` or `DataFrame` objects

We'll cover a couple of these workflows in greater depth.

## This Section's Contents

```{tableofcontents}
```