# Data Wrangling in Pandas

This chapter provides an introduction to reshaping and processing data in Python using Pandas. It reviews foundational syntax for interacting with a `DataFrame` and introduces time series data along with data aggregation and calculation workflows. 

It then moves to data reshaping in Pandas, including operations like `.groupby`, `.pivot`, `.melt`, `.pivot_table`, `.explode`, and `.transpose`. It introduces merging and joining operations in Pandas and includes some discussion of multi-level indexing and regular expressions.

## Acknowledgements

The author consulted the following resources when building this chapter:
- `pandas` package ["Getting started"](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/) documentation.
- [W3Resource Pandas guides](https://www.w3resource.com/pandas/index.php)
- Wes McKinney's [*Python for Data Analysis: Data Wrangling With pandas, Numpy, and IPython*](https://www.oreilly.com/library/view/python-for-data/9781491957653/) (O'Reilly, 2017)
  * Chapter 5 "Getting Started with pandas" (125-168)
  * Chapter 7 "Data Cleaning and Preparation" (195-224)
  * Chapter 8 "Data Wrangling: Join, Combine, and Reshape" (225-256)
  * Chapter 10 "Data Aggregation and Group Operations" (293-322)
  
All figures shown in this lab are from the `pandas` "Getting Started" tutorials.

## Chapter Contents

```{tableofcontents}
```

## Data

We'll work with a few different datasets in this chapter.

- [American Community Survey 1-Year Estimates Public Use Microdata Sample](https://www.census.gov/data/developers/data-sets/census-microdata-api.html)
  - Code for this API call is included

- Air quality data (code is included to load this data from URLs)
  * [`air_quality_no2`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch5/air_quality_no2_long.csv) provies NO<sub>2</sub> values for three measurement stations.
  * [`air_quality_pm25`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch5/air_quality_pm25_long.csv) provides PM<sub>25</sub> values (particulate matter less than 2.5 micrometers) for the same three measurement stations.
  * [`air_quality_stations`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch5/air_quality_stations.csv)  provides latitude and longitude coordinates for five different measurement stations.
  * [`air_quality_parameters`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch5/air_quality_parameters.csv) provides parameter full description and name for five different element types.

- <a href="https://data.census.gov/table/ACSST5Y2022.S1501?t=Education:Educational Attainment&g=050XX00US18141,18141$8600000&moe=false">Educational outcome attribute data from the American Community Survey</a>
  * [Link to download](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch5/data.csv)
  * *Note: I'm working with 2022's 5 year estimate, which I've renamed `data.csv`.*

## Application

[Click here](https://colab.research.google.com/drive/1vYSi18sXN626pFbT7GlHU7TXZLdOtxVJ?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.