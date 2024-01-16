---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.1
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# Elements of Computing (S24): Data Sources (part 1)

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is written by [Katherine Walden](https://github.com/kwaldenphd) and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Acknowledgements

## Table of Contents

## How to Use This Notebook

First, make sure you're working in the copy of the notebook that has your name (check the file name in the top left-hand corner of the screen).

We're using a Python authoring environment called **a notebook**, which is made up of blocks or cells.
- Text cells (like this one), consist of formatted text. For the most part, these cells include instructions and you will just read them.
- Code cells (like the sample one below) have Python code that you will run. To run a code cell, hover over it with the cursor and click the `arrow` icon.

SCREENSHOT

If at any point you want to add a new code cell to try things out on your own, there are a couple ways to add a code cell. First, you'll need to click on a text or code cell near where you want to add a cell:
- `+ Code` in the upper left-hand corner of the screen, under `Help`
- `Insert -> Code cell` in the upper left-hand menu bar

## Lab Notebook Template

Moving forward, we're going to be submitting lab notebooks using the provide Jupyter Notebook template.
- If working in JupyterLab (or another desktop IDE), download the `.ipynb` file to your local computer
  * `File` - `Download` - `Download as .ipynb`
- If working in Google Colaboratory, MAKE SURE you save a copy to your local drive. Otherwise your changes will not be saved.
  * `File` - `Save a copy in Drive`

The lab notebook template includes all of the questions as well as pre-created markdown cells for narrative text answers and pre-created code cells for any programs you may need to create.
- Double click on these cells to edit and add your own content
- If questions do not require a code component, you can ignore those cells
- If questions to not require a narrative component, you can ignore those cells

If working in JupyterLab or another desktop IDE, upload the lab notebook template `.ipynb` file to Canvas as your lab submission.

If working in Google Colaboratory, submit the link to your notebook (checking sharing permissions, similar with Google Docs).

## Overview

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Data_Structures.png?raw=true" width="1000"></p>

In this lab, we're thinking about how Python's built-in data structures (along with `Pandas` workflows) connect to how data is often structured in files or made available on the web.

We'll also be covering how to access data via web APIs, and preliminary workflows for text mining & documents.

## Structured Data

Specifically, we're thinking about a couple key data structures:
- Tabular data, or data stored as a table consisting of rows and columns
- Data stored as name-value pairs, specifically in the JavaScript Object Notation (`.json`) format

<table>
<tr><td><p align="center"><img src="https://github.com/kwaldenphd/python-structured-data/blob/main/images/One_Dimensional_Array.jpg?raw=true" width="500"></p></td><td><p align="center"><img src="https://github.com/kwaldenphd/python-structured-data/blob/main/images/Associative_Arrays.png?raw=true" width="500"></p></td></tr>
	<tr><td align="center">Linear Array</td><td align="center">Associative Array</td></tr></table>

We can connect these two types of data structures back to the concepts of linear and associative arrays covered previously in the course. A quick refresher:
- "In computer science, an array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...The simplest type of data structure is a linear array, also called one-dimensional array" ([Wikipedia, "Array (data structure)](https://en.wikipedia.org/wiki/Array_(data_structure))")
- Associative arrays are "an abstract data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection" ([Wikpedia, Associative Array](https://en.wikipedia.org/wiki/Associative_array))

### Tabular (or Delimited) Data

<p align="center"><img src="https://github.com/kwaldenphd/python-structured-data/blob/main/images/table_diagram.png?raw=true" width="1000"></p>

"A delimited file is a sequential file with column delimiters. Each delimited file is a stream of records, which consists of fields that are ordered by column. Each record contains fields for one row. Within each row, individual fields are separated by column delimiters. All fields must be delimited character strings, non-delimited character strings, or external numeric values. Delimited character strings can contain column delimiters and can also contain character string delimiters when two successive character string delimiters are used to represent one character." (IBM, "[Delimited File Format](https://www.ibm.com/docs/en/db2-for-zos/11?topic=utilities-delimited-file-format)", 5 February 2022)

A few characteristics that distinguish `.csv` files (or other plain-text delimited data formats) from proprietary spreadsheet file types:
- Columns in a `.csv` file don't have a value type. Everything is a string.
- Values in a `.csv` file don't have font or color formatting
- `.csv` files only contain single worksheets
- `.csv` files don't store formatting information like cell width/height
- `.csv` files don't recognize merged cells or other kinds of special formatting (frozen or hidden rows/columns, embedded images, etc.)

### JavaScript Object Notation

START HERE: https://youtu.be/B8AvytgCBdE?si=SIkXF1u7xFOznfv0

<p align="center"><img src="https://github.com/kwaldenphd/python-structured-data/blob/main/images/JSONSample.jpg?raw=true" width="500"></p>

JavaScript Object Notation (JSON) is as popular way to format data as a single (purportedly human-readable) string. JavaScript programs use JSON data structures, but we can frequently encounter JSON data outside of a JavaScript environment.

Websites that make machine-readable data available via an application programming interface (API- more on this soon) often provide that data in a JSON format. JSON structures can vary WIDELY depending on the specific data provider, but the easiest way to think of JSON data as a plain-text data format made up of something like key-value pairs, like we've encountered previously in working with dictionaries (as a type of associative array).

Example JSON string: `stringOfJsonData = '{"name": Zophie", "isCat": true, "miceCaught": 0, "felineIQ": null}'`. From looking at the example string, we can see field names or keys (`name`, `isCat`, `miceCaught`, `felineIQ`) and values for those fields.

To use more precise terminology, JSON data has the following attributes:
- uses name/value pairs
- separates data using commas
- holds objects using curly braces `{}`
- holds arrays using square brackets `[]`

In our example `stringOfJsonData`, we have an object contained in curly braces. An object can include multiple name/value pairs. Multiple objects together can form an array.

How is data stored in a JSON format different than a `.csv`?
- A `.csv` file uses characters as delimiters and has more of a tabular (table-like) structure.
- `.json` data uses characters as part of the syntax, but not in the same way as delimited data files.
- The data stored in a JSON format has values that are attached to names (or keys).
  * NOTE: We can mimic this structure somewhat by loading a `.csv` as a dictionary data structure
- JSON can also have a hierarchical or nested structure, in that objects can be stored or nested inside other objects as part of the same array.

### Loading Structured Data in Python

Much of our work this semester will utilize `Pandas`, a powerful Python library for working with structured data. But we can also work with structured data using Python's built-in secondary data structures and the `csv` and `json` modules.

#### Without Pandas

##### `csv`

The `csv` module allows us to create a `reader` object that iterates over lines in a `.csv` file. We can use it to read or load an existing `.csv` file into Python. 

```Python
# loading delimited data as list of lists
import csv # import statement
file = open('example.csv') # open file
reader = csv.reader(file) # create reader object
data = list(reader) # create list of lists
print(data) # show output
```

```Python
# if we wanted to combine those steps
import csv # import statement
data = list(csv.reader(open('example.csv'))) # open file, create reader object, convert to list
print(data) # show output
```

For more on using the `csv` module and this workflow:
- [Elements of Computing I lab notes](https://github.com/kwaldenphd/python-structured-data/tree/main#read)

```Python
# loading delimited data as dictionary
import csv # import statement
file = open('example.csv') # open file
dictReader = csv.DictReader(file) # DictReader object
data = list(dictReader) # convert DictReader to list of dictionaries
print(data) # show output
```

```Python
# if we wanted to combine those steps
import csv # import statement
data = list(csv.DictReader(open('example.csv'))) # open file, create DictReader object, convert to list of dictionaries
print(data) # show output
```

##### `json`

We can read JSON into Python using the `json` module, which includes a few key functions for loading JSON data into Python:
- `json.loads()` takes a single string of JSON and loads it as a Python value
- `json.load()` takes a JSON file (or file-like object) and loads it as a Python value
- `json.dumps()` takes a Python value and transforms it to a JSON object.

Values stored in JSON format must be one of the following data types:
- string
- number
- object (JSON object)
- array
- boolean
- null

Translation table for how Python's `json` module interprets or renders these data types:

JSON | Python
--- | ---
object | dict
array | list
string | str
number (int) | int
number (real) | float
true | True
false | False
null | None

To translate a string of JSON data into a Python value, we pass it to the `loads()` function contained in the `json` module.

```Python
import json # import statement
jString = '{"name": "Zophie", "isCat": true, "miceCaught": 0, "felineIQ": null}' # string of JSON data
data = json.loads(jString) # load JSON data as Python value
print(data) # show output
```

When loading a JSON file (or file-like object), we would need to use the `json.load()` argument.

```Python
import json # import statement
file = open("example.json") # open file
data = json.load(file) # parse as JSON
print(data) # show output
```

For more on using the `json` module and this workflow:
- [Elements of Computing I lab notes](https://github.com/kwaldenphd/python-structured-data/tree/main#javascript-object-notation)

If you're feeling fuzzy on file methods:
- [Elements of Computing I lab notes](https://github.com/kwaldenphd/python-structured-data/tree/main#overview)

#### With Pandas

<p align="center"><img src="https://github.com/kwaldenphd/pandas-intro/blob/main/images/series_df_diagram.png?raw=true" width="1000"></p>

`pandas` has two main data structures: `Series` and `DataFrame`.
- "A `Series` is a one-dimensional, array-like object containing a sequence of values...and an associated array of data labels, called its index" (McKinney, 126)
- A `DataFrame` includes a tabular data structure "and contains an ordered collection of columns, each of which can be a different value type" (McKinney, 130).

##### Delimited file -> `DataFrame`

Loading a delimited file as a DataFrame is fairly straightforward.

```Python
import pandas as pd # import statement
df = pd.read_csv("example.csv") # load file, create dataframe
print(df) # show output
```

`.read_csv()` can include a number of other arguments or parameters to handle different data loading challenges, for example other delimiter characters, escape characters, and data type conversion. For more on parsing delimited data in `Pandas`:
- [Pandas documentation](https://pandas.pydata.org/docs/user_guide/io.html)

The `read_` prefix can be used with other structured data file formats. For more on `Pandas` and file I/O:
- [Pandas documentation](https://pandas.pydata.org/docs/user_guide/io.html)

##### `Pandas` & `JSON`

Since a `DataFrame` is a flat two-dimensional structure, highly-nested JSON can present a challenge.

Pandas includes a few JSON-specific functions. Documentation links are included below.
- [Reading JSON](https://pandas.pydata.org/docs/user_guide/io.html#reading-json)
- [.read_json()](https://pandas.pydata.org/docs/reference/api/pandas.read_json.html)
- [.json_normalize()](https://pandas.pydata.org/docs/reference/api/pandas.json_normalize.html#pandas.json_normalize)

We'll come back to these functions when we start working with web API returns.

### Application

Q1A: Navigate to an open data portal and download a `.csv` file. 

A few places to start:
- [Data.gov](https://www.data.gov/)
- [City of Chicago Data Portal](https://data.cityofchicago.org/)
- [City of South Bend Open Data](https://data-southbend.opendata.arcgis.com/)

These open data portals are catalogs of datasets- you will need to explore the websites to identify and then download a specific dataset.

Open the data in a spreadsheet program and/or text editor. 
- What do you see?
- How can we start to make sense of the data based on available documentation?

Q1B: Write three programs that load the data in Python using the different approaches highlighted in the previous section of the lab:
- Lists and sublists
- Dictionaries
- Pandas `DataFrame`

Answer to this question includes program + comments that document process and explain your code.

Q1C: What challenges did you encounter? How did you address or solve them? 

+++

Q2A: Navigate to an open data portal and download a JSON file. 

Some options that can get you started:
- [Data.gov](https://www.data.gov/)
- [City of Chicago Data Portal](https://data.cityofchicago.org/)
- [City of South Bend Open Data](https://data-southbend.opendata.arcgis.com/)

These open data portals are catalogs of datasets- you will need to explore the websites to identify and then download a specific dataset. 

Q2B: Open the data in a spreadsheet program and/or text editor. Describe what are you seeing. How can we start to make sense of this data? What documentation is available?

Q2C: Write a program that loads the JSON data into Python, using the workflow shown in the previous section of the lab.
- You're welcome to explore creating a Pandas `DataFrame`, but that's not required.

Answer to this question includes program + comments that document process and explain your code.

Q3C: What challenges did you encounter? How did you address or solve them? 

## Web APIs

START HERE (YouTube): https://youtu.be/qW1qhb8r8xI?si=q8jdyE6oZEsH4xFR

For a brief introduction to APIs, view Danielle Thé, ["API's Explained (with LEGO)"](https://youtu.be/qW1qhb8r8xI), *YouTube Video* (1 November 2016).

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

### API Terminology & General Workflow

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

### City of South Bend Open Data Portal

OPEN DATA PORTAL SCREENSHOT

Head to the City of South Bend's Open Data Portal. Identify a specific dataset you want to load in Python.

DATA INVENTORY SCREENSHOT

I'm working with the raw data from the City's 2022 Digital Literacy Survey.
- https://data-southbend.opendata.arcgis.com/datasets/SouthBend::2022-digital-literacy-survey-raw-data/about

VIEW API RESOURCES SCREENSHOT

We could download this data as a `CSV` file, but let's instead explore the API options.

API EXPLORER SCREENSHOT

https://data-southbend.opendata.arcgis.com/datasets/SouthBend::2022-digital-literacy-survey-raw-data/api

QUERY URL SCREENSHOT 

Spend some time exploring the options on this page. As you customize the query, notice how the `Query URL` changes. We can think about the `URL` as the data's "address." Modifying what data we want requires modifying the address.

Once you have finalized your query (what parts of this data you want to work with in Python), we'll use the `requests` and `json` modules to load the data.

```Python
import requests, json # import statements
r = requests.get("https://opendata.arcgis.com/datasets/c97085b608604f5c8c07487c24dcaff4_0/FeatureServer/0/query?where=1%3D1&outFields=*&outSR=4326&f=json") # request data from url
data = r.json() # parse response as JSON object
print(data) # show output
```

We can use Python dictionary syntax to make sense of what's in this output.

```Python
# show top-level keys
print(data.keys())
```

At first glance, everything up through the `fields` key looks like technical information about the API return. `fields` doesn't have the survey responses, but it does have important metadata about the survey data.

Let's start by creating a `DataFrame` with this `metadata` (data about data).

```Python
metadata = pd.DataFrame(data['fields']) # create dataframe
metadata.to_csv("metadata.csv", index=False) # write metadata to csv file
print(metadata) # show output
```

The `fields` key includes survey response data, but it's structured as a list of dictionaries. We'll need to use a combination of list and dictionary Python syntax (and some trial and error) here.

```Python
print(type(data['features'])) # shows us data type for the value associated with the features key
```

```Python
response = data['features'][0] # selects the first response
print(type(response)) # show response data type
```
```Python
print(response.keys()) # shows keys for single response
```
```Python
print(type(response['attributes'])) # show data type for attributes value
```
```Python
print(response['attributes'].keys()) # gets value for attributes key, shows those keys
```

That's starting to look like survey results. We could use another print statement to confirm.

```Python
for key, value in response['attributes'].items(): # iterate over dictionary items
  print(key, value) # show key and value
```

Now that we understand how the API return data is structured, we can create a `DataFrame` with the survey data. We'll first need a list with the survey response dictionaries.

```Python
import pandas as pd # import statement

surveyData = [] # empty list for responses

for d in data['features']: # iterate over list of dictionaries
  surveyData.append(d['attributes']) # isolate value and append to list

df = pd.DataFrame(surveyData) # create df
print(df) # show output
```

Now, there's more we might want to do with this `DataFrame` (rename columns, remove unneeded columns, perform other kinds of calculations, etc). But this gets us started!

To recap what we just did:
- Customize query URL
- Load response in Python
- Parse the data structure to isolate the data we want
- Store that data as a Pandas `DataFrame`

#### Application

Q3: 

Work through this for another open data portal dataset. You're welcome to use another City of South Bend dataset, and it's fine to continue with the Q1 dataset. 

But if you want to flex you API muscles, try a different open data portal to learn a new interface and data structure! Lots to choose from, but Chicago and NYC are good places to start.
- [Chicago Data Portal](https://data.cityofchicago.org/)
  * [Documentation](https://dev.socrata.com/docs/endpoints.html)
- [NYC Open Data](https://opendata.cityofnewyork.us/)
  * [Documentation](https://dev.socrata.com/docs/endpoints.html) 

Starting to make sense of the documentation

Getting the data in Python

Storing as pandas df

### U.S. Census Bureau

As we've seen previously, the U.S. Census Bureau collects a wealth of information about people, households, communities, etc. They also have a [number of APIs](https://www.census.gov/data/developers/data-sets.html) and a [robust user community](https://www.census.gov/data/what-is-data-census-gov/guidance-for-data-users/how-to-materials-for-using-the-census-api.html).

<p align="center"><a href="https://github.com/kwaldenphd/apis-python/blob/main/Figure_2.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/apis-python/blob/main/Figure_2.png?raw=true" /></a></p>

Unlike the APIs we encountered in the previous section of the lab, the Census Bureau's API requires a key. Head to the Census Bureau's ["About"](https://www.census.gov/data/developers/about.html) page for developers and click the "Request a Key" icon. Once you've completed the "Request a Key" form, you should receive an API key via email. This will look like a long string of letters and numbers.
- *It's fine to use your name or "University of Notre Dame" for "Organization Name"*

#### Selecting a Dataset

TABLE INVENTORY SCREENSHOT

The first step is figuring out what Census Bureau dataset and API you want to work with. One option is to use [data.census.gov](https://data.census.gov/)'s data explorer interface. Keyword search results can point you to datasets of interest (which you would then have to track down in the API documentation).

AVAILABLE APIS SCREENSHOT

https://www.census.gov/data/developers/data-sets.html

Looking at the APIs for [specific Census Bureau data collection instruments](https://www.census.gov/data/developers/data-sets.html) is also a place to start. 

DOISCOVERY TOOL SCREENSHOT 

You could also jump into the [API Discovery Tool](https://www.census.gov/data/developers/updates/new-discovery-tool.html), which is available in a couple different formats. This is a machine-readable inventory of Census Bureau datatasets. It can also be slightly overwhelming.

For this example, I'm going to use microdata from the American Community Survey, specifically the "[2022 American Community Survey 1-Year Estimates Public Use Microdata Sample (2005-2019, 2021, 2022)](https://www.census.gov/data/developers/data-sets/census-microdata-api.ACS_1-Year_PUMS.html#accordion-container-accordion-4ad4d2b1b3)."
- [Link to the API documentation](https://www.census.gov/data/developers/data-sets/census-microdata-api.ACS_1-Year_PUMS.html#accordion-container-accordion-4ad4d2b1b3)

#### Constructing Your Query

Before you jump into writing the API call in Python, use the available documentation to make sense of how the URL is structured, what variables are included in the dataset, etc. 

Note that for the Census Bureau API, your key is part of the URL. Concatenation and a string variable can be helpful here.

Let's break down one of the example URLs included in the documentation for this survey.

```
https://api.census.gov/data/2022/acs/acs1/pums?get=SEX,PWGTP,MAR&SCHL=24&key=YOUR_KEY_GOES_HERE
```

We can start to break down the pieces of information included here:
- Root: `https://api.census.gov/data`
- Survey: `acs` (American Community Survey)
- Coverage: `acs1` (1 year estimates)
- Subset: `pums` (Public Use Microdata Sample)
- Query: `?get=` (prefix for selecting specific variables)
- Variables: `SEX,PWGTP,MAR&SCHL=24` (codes for specific variables, from [the documentation](https://api.census.gov/data/2022/acs/acs1/pums/variables.html))
  * NOTE: In this example, the URL is structured to select all values for the `SEX`, `PWGTP`, `MAR` variables. This query will only return records where the `SCHL` variable value is `24`.
  * In a scenario where we are not filtering for specific variable values, we could just include variable names separated by commas (i.e. `SEX, PWGTP, MAR, SCHL`)
- `&key=` (prefix for entering your API key)

#### Writing the API Call

Remember our general API workflow:
- Customize query URL
- Load response in Python
- Parse the data structure to isolate the data we want
- Store that data as a Pandas `DataFrame`

```Python
import requests, pandas as pd # import statements
key = "" # add your key to make this a string variable
url = f"https://api.census.gov/data/2022/acs/acs1/pums?get=SEX,PWGTP,MAR&SCHL=24&key={key}" # use f strings and concatenation to construct the query
r = requests.get(url) # requests data
data = r.json() # store response
df = pd.DataFrame(data[1:], columns=data[0]) # create the dataframe, making the first sublist the column headers, and starting with the first row of data to avoid duplicating headers)
print(df) # show output
```

#### Other Resources

This is an example query- there are lots of ways to customize Census Bureau API requests. Check out [`census-docs`](https://census-docs.com/) and the Census Bureau's API documentation for more info.
- For example, if we just wanted data for Indiana, we could add the `in` parameter to your URL: 'api.census.gov/data/2022/acs/acs1/pums?get=SEX,PWGTP,MAR&SCHL=24&in=state:17&key=`

Some datasets include `Groups`, which let you return multiple related variables.
- [Link to more information on groups](https://www.census.gov/data/developers/updates/groups-functionality.html)

DataMade also has a Python wrapper for the Census Bureau APIs, which is designed to streamline programming workflows.
- [Link to more information](https://github.com/datamade/census)

The Census Bureau APIs can be overwhelming, but they're a powerful tool for accessing data. Wading through the documentation is worth your time.

#### Application 

+++

Q4: 

Write your own Census Bureau API call. You could use the same dataset and modify the year, variables, geography scope, etc.

You could also explore other datasets.

Starting to make sense of the documentation

Getting the data in Python

Storing as pandas df

## Working With Unstructured Text

START HERE
- Elisevier video: https://youtu.be/I3cjbB38Z4A?si=N3hv-j7dkOHDkXED
- Elsivier video: https://youtu.be/xxqrIZyKKuk?si=ncOxIy5EZufVpmkf

EXPLANATION FOR UNSTRUCTURED TEXT

If you took Elements of Computing I with Prof. Walden, you had some exposure to how we can start to work with unstructured text, looking at things like term relationships, frequency, etc. Web scraping is a great workflow for information that is online in web pages. But what about text information contained in documents? 

Enter Optical Character Recognition, or OCR.

"Optical character recognition (OCR) is sometimes referred to as text recognition. An OCR program extracts and repurposes data from scanned documents, camera images and image-only pdfs. OCR software singles out letters on the image, puts them into words and then puts the words into sentences, thus enabling access to and editing of the original content...OCR systems use a combination of hardware and software to convert physical, printed documents into machine-readable text" (IBM Cloud Education, "[What is Optical Character Recognition?](https://www.ibm.com/blog/optical-character-recognition/)", 5 January 2022)

OCR is an example of computer vision in action. A full exploration of OCR or computer vision is outside the scope of this course. We're going to focus on some Python workflows for extracting text and data from PDF documents that already contain text.
- [Link to a (messy) Jupyter Notebook that walks through some OCR foundations](https://drive.google.com/file/d/1WbGTAvs1WCGrC5XZeADyhminFn8QMEHT/view?usp=sharing)

We're going to be using a couple Python libraries built for extracting text and tables from PDF files.
- [`pypdf`](https://pypdf.readthedocs.io/en/stable/index.html)
- [`tabula-py`](https://tabula-py.readthedocs.io/en/latest/)

And we'll be testing out these workflows on a PDF file from the [City of South Bend's Document Search Center](http://docs.southbendin.gov/WebLink/Welcome.aspx?cr=1). I'm looking at the [Inclusive Procurement & Contracting Board's 2020 report](http://docs.southbendin.gov/WebLink/0/edoc/335114/2020%20Annual%20Inclusion%20Contracting%20Procurement%20Report%203-27-21_.pdf).

### Python Workflows

We'll start by installing and importing these packages.

```Python
!pip install pypdf tabula-py
```

```Python
# import statements
from pypdf importPdfReader
import tabula
```

Next, we'll use `PdfReader` to extract text.

```Python
reader = PdfReader("pdf20.pdf") # load renamed file as reader object
page = reader.pages[2] # isolate single page
print(page.extract_text()) # show extracted text output
```

To iterate over all pages in the document and write the contents to a `.txt` file:

```Python
with open("output.txt", "a") as f: # create file
  for p in reader.pages: # iterate over pages
    f.write(p.extract_text()) # extract text and write to file
```

Folks may be wondering how we might handle tables or tabular data in a PDF file. We can use Tabula's `.read_pdf()` function to extract all tables in our document as Pandas `DataFrames`.

```Python
dfs = tabula.read_pdf("pdf20.pdf", pages="all") # load file, isolate dataframes
dfs[5].to_csv("output.csv", index=False) # write single dataframe to CSV file
dfs[5] # show single dataframe
```

There's more we probably want to do with output, but this gets us started.

### Application

Q5:

Find another SB file. 

Skim the document, what types of information are there.

Extract text to txt file

Extract tables, write one to CSV file

Where you'd want to go next, other data processing steps

## How to Submit This Lab & Show Your Work

## Lab Notebook Questions
`
