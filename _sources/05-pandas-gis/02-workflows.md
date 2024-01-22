# Geospatial Data Workflows

Calculating latitude and longitude or drawing polygons from scratch is outside the scope of this course. But thankfully many resources exist to help with these workflows.

## Geocoding

<blockquote>"Geocoding is the process of transforming a description of a location—such as a pair of coordinates, an address, or a name of a place—to a location on the earth's surface." (ArcGIS Desktop, "<a href="https://desktop.arcgis.com/en/arcmap/latest/manage-data/geocoding/what-is-geocoding.htm">What is geocoding?</a>")</blockquote>

In a scenario where you need to add latitude and longitude, there are a number of free online resources and Python libraries that support geocoding.

Free online geocoding services:
- [LocalFocus data journalism batch geocoder](https://geocode.localfocus.nl/)
- [Texas A&M Geocoding Services](https://geoservices.tamu.edu/Services/Geocode/)
  * *Requires creating a free account*
 
There are also Python libraries that support geocoding.
- [`GeoPy`](https://geopy.readthedocs.io/en/stable/)
- [`Geocoder`](https://geocoder.readthedocs.io/providers/Mapbox.html) (requires a free Mapbox API key)
- Abdishakur, ["Geocode with Python"](https://towardsdatascience.com/geocode-with-python-161ec1e62b89) *Towards Data Science* (15 September 2019)

## Boundary Files

Many civic and government data intermediaries publish `boundary files`, or geospatial data files that include metadata for area polygons. 

This data is typically some type of JSON structure, and published in a few common file types.
- `KML` (keyhole markup language, includes tags with elements and attributes)
- `GeoJSON` (geospatial JSON data)
- `SHP` (shapefile, a proprietary format)

A few resources that are good starting points:
- [St. Joseph County GIS Hub](https://www.sjcindiana.com/1743/GIS--County-Mapping)
- [U.S. Census Bureau Cartographic Boundary Files](https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html)