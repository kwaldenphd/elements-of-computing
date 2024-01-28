# Interactive Mapping

`plotly` supports two different types of maps.
- ***Mapbox maps*** are tile-based maps that are rendered using tiles that join together to form the map plot.
- ***Geo maps*** are outline-based maps that are rendered using the `layout.geo` object  that contains map configuration information.

Both of those map types support point and polygon data.

<table><tr><th></th><th>Point Data</th><th>Polygon Data</th></tr>
<tr><th>Outline Map (or Geo Map)</th><td>Draw a base map / base layer<br>Point data is similar to a scatter plot<br><code>px.scatter_geo()</code></td><td>Draw base map / base layer with polygons<br>Join attribute data to the polygons<br><code>px.choropleth()</code></td></tr>
<tr><th>Tile (or mapbox) map</th><td>Use mapbox tiles for base map / base layer<br>Point data is similar to a scatter plot<br><code>px.scatter_mapbox()</code></td><td>Use mapbox tiles for base map / base layer<br>Join attribute data to the polygons<br><code>px.choropleth_mapbox()</code></td></tr></table>

## Section Table of Contents

```{tableofcontents}
```