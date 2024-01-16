# Web APIs

<iframe width="560" height="315" src="https://www.youtube.com/embed/qW1qhb8r8xI?si=11aJZ9_6zB9dQ-gu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Start by watching a 4 minute video overview of APIs.
- [YouTube link](https://youtu.be/qW1qhb8r8xI?si=q8jdyE6oZEsH4xFR)

<p align="center"><a href="https://github.com/kwaldenphd/apis-python/blob/main/Figure_1.jpg?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/apis-python/blob/main/Figure_1.jpg?raw=true" /></a></p>

We're focusing on web APIs, which allow for information or functionality to be manipulated by other programs via the internet. Web APIs are a popular workflow for making data available from large-scale repositories. A few examples...

- The U.S. National Archives and Records Administration (NARA) makes the National Archives catalog, Executive Orders, and photographic image content available [via an API](https://www.archives.gov/developer#toc--datasets).
- The Smithsonian Institution allows open access to museum collection metadata [via an API](https://www.si.edu/openaccess/devtools).
- The U.S. Library of Congress provides access to digital collection metadata, digitized historical newspaper images, public radio and television programs, and World Digital Library collections [via APIs](https://labs.loc.gov/lc-for-robots/). 
- The U.S. Census Bureau makes a wide range of public data available [via API](https://www.census.gov/data/developers/data-sets.html).

APIs let us bring a live data connection into a programming environment and interact or work with it based on the format and protocols established as part of the API.

For example, imagine you want to know winter weather road conditions or the status of snow plow routes. Downloading a static dataset isn't going to work for this specific use case--you need a live data feed with up-to-date information. This is the beauty of APIs!
- [Track down Iowa Department of Transportation's nearly 901 snow plows](https://public-iowadot.opendata.arcgis.com/pages/winter). 
- [Link to IDOT's plow truck data](https://public-iowadot.opendata.arcgis.com/datasets/IowaDOT::snow-plow-truck-location-avl-iowa-dot/about)


## API Terminology & General Workflow

Some terminology that goes along with APIs.
- ***HTTP (HyperText Transfer Protocol)***: primary means of communicating or transferring data on the world wide web. 
- ***URL (Uniform Resource Locator)***: an address or location information for information on the web. A URL describes the location of a specific resource.
- ***JSON (JavaScript Object Notation)***: plain-text data storage format
- ***REST (REpresentational State Transfer)***: best practices for implementing APIs. APIs that follow these principles are called REST APIs.

A very general web API workflow....
- Request data from a URL
  * Sometimes you have to specify additional parameters, like headers or an access key/token.
- Store the response in Python
- Convert the response to the appropriate Python data structure

Let's look at a couple of examples. 

## Section Table of Contents

```{tableofcontents}
```