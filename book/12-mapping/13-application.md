# Application

[Click here](https://colab.research.google.com/drive/1igToXStJBCZGqutfIXu2b_3MJFO6SOmO?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

All the materials to reproduce your work (notebook and data files, API call, etc) should be included in the assignment Google Drive folder.

## Geocoding

If you're working with point data that does not have geospatial attributes (latitude and longitude), you'll need to add that information via a process called geocoding.

Free online geocoding services:
- [LocalFocus data journalism batch geocoder](https://geocode.localfocus.nl/)
- [Texas A&M Geocoding Services](https://geoservices.tamu.edu/Services/Geocode/)
  * *Requires creating a free account*
 
There are also Python libraries that support geocoding.
- [`GeoPy`](https://geopy.readthedocs.io/en/stable/)
- [`Geocoder`](https://geocoder.readthedocs.io/providers/Mapbox.html) (requires a free Mapbox API key)
- Abdishakur, ["Geocode with Python"](https://towardsdatascience.com/geocode-with-python-161ec1e62b89) *Towards Data Science* (15 September 2019)

## Geometry Information 

If you're working with polygon data or attribute data that connects to polygons, you'll need to connect (merge or join) your attribute data with geometry information.
- Option #1: Boundary files 
  * A number of different places to access free boundary files. When available, a `GeoJSON` format may be the most user-friendly.
    * [IPUMS](https://international.ipums.org/international/gis.shtml) (international; first, second, third level geographies)
    * [U.S. Census Bureau](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html) (U.S. states and geographic regions)
- Option #2: Built-in geometries
  * Mapping tools like Plotly or GeoPandas have some built-in geometries. Documentation is your friend.
    * [Plotly](https://plotly.com/python/choropleth-maps/)
	* [GeoPandas](https://geopandas.org/en/stable/gallery/plotting_basemap_background.html)
- Option #3: Web servers
  * We've seen a few different examples in this chapter around options for bringing in tile-based maps and geometry information. Often similar to working with a web API.

## Question

**Q1A: Identify an aspect of your final project data (or another civic dataset) that has a geospatial component. This could be involve neighborhoods, districts, zip codes, addresses, etc. Answer to this question notes the attribute dataset you're working with and what aspects of it you want to analyze.**

**Q1B: Develop an outline for your data analysis workflow. This could be a list with bullet points, a narrative, or a visual diagram (or a combination of these elements). Answer to this question includes notes on a desired final data structure and preliminary outputs.**
- *NOTE: No code is required as part of this answer.*

**Q1C: Develop a Python program that uses mapping functions covered in this chapter to generate at least three different maps using your Q1A dataset and Q1B workflows. Answer to this question includes code + comments.**
- *I encourage folks to use this question to explore visualizations you might use for the final project.*

Each plot should include the following elements:
- Title
- Hover labels (if building an interactive map)
- Scale or legend
- Data source

Types of interactive maps to choose from:
- Geo Maps, or Outline-Based Maps
  * Point map, `px.scatter_geo()`
  * Choropleth map `px.choropleth()`
- Mapbox or Tile-Based Maps
  * Point map, `px.scatter_mapbox()`
  * Choropleth map, `px.choropleth_mapbox()`
  
For more on static maps: 
- ["Visualizing Data in GeoPandas"](https://kwaldenphd.github.io/elements-of-computing/12-mapping/04-geopandas-viz.html) page from this chapter

**Q1D: What challenges did you encounter? How did you approach solving them?**
