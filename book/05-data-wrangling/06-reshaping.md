# Reshaping Data

We've already covered how to sort or group by values in a dataframe. We can also perform more drastic data manipulations and transformations using `pandas`.

A digest of these operations, courtesty of [Pandas documentation](https://pandas.pydata.org/docs/user_guide/reshaping.html):
* `pandas.pivot` and `pandas.pivot_table`: Group unique values within one or more discrete categories.
* `DataFrame.stack` and `DataFrame.unstack`: Pivot a column or row level to the opposite axis respectively.
* `pandas.melt` and `pandas.wide_to_long`: Unpivot a wide `DataFrame` to a long format.
* `pandas.get_dummies` and `pandas.from_dummies`: Conversions with indicator variables.
* `Series.explode`: Convert a column of list-like values to individual rows.
* `pandas.crosstab`: Calculate a cross-tabulation of multiple 1 dimensional factor arrays.
* `pandas.cut`: Transform continuous variables to discrete, categorical values
* `pandas.factorize`: Encode 1 dimensional variables into integer labels.

We'll cover some of these workflows in greater depth.

## Hierarchical Indexing, or MultiIndex

<p align="center"><img src="https://miro.medium.com/v2/resize:fit:1400/1*bvMuj1LBKcLwwwyQYnarpw.png" width="1000"></p>

As part of these workflows, we'll see the different ways `Pandas` supports hierarchical indexing, sometimes called a multi-index.

Multiple rows or columns can be part of a `DataFrame`'s indices.

For more detailed information:
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/03.05-hierarchical-indexing.html)
- [Pandas documentation](https://pandas.pydata.org/docs/user_guide/advanced.html)

## This Section's Contents

```{tableofcontents}
```