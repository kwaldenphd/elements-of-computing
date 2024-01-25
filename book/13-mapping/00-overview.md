# Mapping

Up to this point, we have been working with data plotted on a 2D cartesian coordinate system, with x and y axes. For our purposes, it's most useful to think of maps in the same way--as data plotted on a coordinate system. Except for maps, that coordinate system is typically some type of latitude or longitude based projection, and the data to be plotted includes explicit location information (rather than a numerical or categorical field that can be mapped to an axis).

This chapter focuses on workflows for visualizing geospatial data in Python. It covers static visualization workflows with `GeoPandas` and interactive visualization workflows with `plotly`.

## Chapter Contents

```{tableofcontents}
```

## Data 

This chapter uses three datasets:
- [St. Joseph County zip code boundary file](https://sjcgis-stjocogis.hub.arcgis.com/datasets/stjocogis::zip-code-boundaries-3/about)
- <a href="https://data.census.gov/table/ACSST5Y2022.S1501?t=Education:Educational Attainment&g=050XX00US18141,18141$8600000&moe=false">Educational outcome attribute data from the American Community Survey</a>
- [Park location and feature data from the City of South Bend](https://data-southbend.opendata.arcgis.com/datasets/SouthBend::parks-locations-and-features/about)

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