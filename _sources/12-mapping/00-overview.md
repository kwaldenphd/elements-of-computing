# Mapping

Up to this point, we have been working with data plotted on a 2D cartesian coordinate system, with x and y axes. For our purposes, it's most useful to think of maps in the same way--as data plotted on a coordinate system. Except for maps, that coordinate system is typically some type of latitude or longitude based projection, and the data to be plotted includes explicit location information (rather than a numerical or categorical field that can be mapped to an axis).

This chapter provides an introduction to geospatial data, including structures and formats, with a focus on Python programming workflows. It also covers static visualization workflows with `GeoPandas` and interactive visualization workflows with `plotly`.

## Acknowledgements

The author consulted the following resources when developing this chapter:
- Bonny P. McClain, [*Python for Geospatial Data Analysis: Theory, Tools, and Practice for Location Intelligence*](https://www.oreilly.com/library/view/python-for-geospatial/9781098104788/) (O'Reilly, 2022).
- GeeksForGeeks, "[Working With Geospatial Data in Python](https://www.geeksforgeeks.org/working-with-geospatial-data-in-python/)" (n.d.)
- Henrikki Tenkanen, "[Spatial Analysis With Python](https://sustainability-gis.readthedocs.io/en/latest/lessons/L1/intro-to-python-geostack.html)" in [*Spatial Data Science for Sustainable Development*](https://sustainability-gis.readthedocs.io/en/latest/index.html)
- GeoPandas, "[Introduction to GeoPandas](https://geopandas.org/en/stable/getting_started/introduction.html)"

## Chapter Contents

```{tableofcontents}
```

## Data 

We'll be working with a few different datasets in this chapter.

- St. Joseph County zip code boundary file.
  * [Download from source](https://sjcgis-stjocogis.hub.arcgis.com/datasets/stjocogis::zip-code-boundaries-3/about)
  * [Download from GitHub](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch12/zip.geojson)
    * *Note: I've renamed this file `zip.geojson`.*

- <a href="https://data.census.gov/table/ACSST5Y2022.S1501?t=Education:Educational Attainment&g=050XX00US18141,18141$8600000&moe=false">Educational outcome attribute data from the American Community Survey</a> with the St. Joseph County zip code boundary file.
  * [Download file from GitHub](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch12/data.csv)
    * *Note: I'm working with 2022's 5 year estimate, which I've renamed `data.csv`.*

- [Park location and feature data from the City of South Bend](https://data-southbend.opendata.arcgis.com/datasets/SouthBend::parks-locations-and-features/about)
  * [Download file from GitHub](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch12/parks.csv)
    * *Note: I've renamed this file `parks.csv`.*

Sample datasets from the `plotly` library. Code to load these datasets is included.
  * `2014 U.S. Cities Population`
  * `Gapminder Data`
  * `NYC Uber Rides`
  * `U.S. Unemployment Data`
  * `GeoJSON U.S. County Boundaries`

## Mapbox Access Token

Later in this chapter, we'll be working with features of the Mapbox API that require an access token.

Sign up for a free Mapbox account:
- https://account.mapbox.com/auth/signup/

Once you have signed up and logged in, click `Token` in the top level menu (between `Dashboard` and `Statistics`).
- https://account.mapbox.com/access-tokens/

Click the `Create a token` button to create a new access token:
- https://account.mapbox.com/access-tokens/create

Choose a descriptive name for your token ("Elements of Computing" works fine). The default settings for which boxes are checked/unchecked are fine.

Click the `Create token` button at the bottom of the page.

Save this token value (string of numbers and letters) for later in the chapter.

## Application

[Click here](https://colab.research.google.com/drive/1Oz7GGpg5jqchdPTk7_4IrYKf8EuyDoM-?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.