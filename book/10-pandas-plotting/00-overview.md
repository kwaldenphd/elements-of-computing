# Plotting With `Pandas`

This chapter covers how to generate `matplotlib` plots for data stored in a `pandas` `DataFrame`. It provides an overview of how to generate a variety of common plot types, including line plots, bar charts, histograms, box plots, area plots, scatter plots, and pie charts. It also covers how `pandas`'s plotting function handles missing data. 

It provides a comparison of the `matplotlib` and `seaborn` plotting packages and provides an introduction to `seaborn` with sample code. 

## Acknowledgements

The author consulted the following resources when writing  this tutorial:
- Chapter 4.14 "Visualization With Seaborn" from Jake VanderPlas, [*Python Data Science Handbook: Essential Tools for Working with Data*](https://jakevdp.github.io/PythonDataScienceHandbook/04.14-visualization-with-seaborn.html ) (O'Reilly, 2016)
- `pandas`, [User Guide, "Visualization"](https://pandas.pydata.org/docs/user_guide/visualization.html)
- `pandas`, [Getting Started, "Plotting"](https://pandas.pydata.org/docs/getting_started/intro_tutorials/04_plotting.html)
- Chapter 9 "Plotting and Visualization" from Wes McKinney, [*Python for Data Analysis: Data Wrangling With pandas, Numpy, and IPython*](https://www.oreilly.com/library/view/python-for-data/9781491957653/) (O'Reilly, 2017)
- Chapter 15 "Generating Data" from Eric Matthes, [*Python Crash Course: A Hands-On, Project-Based Introduction to Programming*](https://ehmatthes.github.io/pcc/) (No Starch Press, 2019).
- [`seaborn` package documentation](https://seaborn.pydata.org/introduction.html)

## Chapter Contents

```{tableofcontents}
```

## Data 

This chapter uses a few different datasets:

- [Air quality data](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch10/air_quality_no2.csv)
  * Code to load from URL is included

- [City of South Bend budget data](https://data-southbend.opendata.arcgis.com/search?q=budget)
  * Code to load/process this data is included

- We'll also use some data generated randomly with `numpy`. Code to generate random data is included.

- The `seaborn` section of the chapter uses sample datasets that are included in the library.
  * `tips`
  * `dots`

## Application

[Click here](https://colab.research.google.com/drive/1cOshaiEA5eHhJDOi22_x3GRHsxqC0L3_?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.