# Application

[Click here](https://colab.research.google.com/drive/1UrwPsv7GeHKKfKgjOPDK6cAPrco6R2fD?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

## Question 1

**Q1A: Navigate to an open data portal and download a `.csv` file.**

A few places to start:
- [Data.gov](https://www.data.gov/)
- [City of Chicago Data Portal](https://data.cityofchicago.org/)
- [City of South Bend Open Data](https://data-southbend.opendata.arcgis.com/)

These open data portals are catalogs of datasets- you will need to explore the websites to identify and then download a specific dataset.

**Q1B: Open the data in a spreadsheet program and/or text editor.**
- What do you see?
- How can we start to make sense of the data based on available documentation?

**Q1C: Write three programs that load the data in Python using the different approaches highlighted in this chapter:**
- Lists and sublists
- Dictionaries
- Pandas `DataFrame`

Answer to this question includes program + comments that document process and explain your code.

**Q1D: What at challenges did you encounter? How did you address or solve them?**

## Question 2

**Q2A: Navigate to an open data portal and download a JSON file.**

Some options that can get you started:
- [Data.gov](https://www.data.gov/)
- [City of Chicago Data Portal](https://data.cityofchicago.org/)
- [City of South Bend Open Data](https://data-southbend.opendata.arcgis.com/)

These open data portals are catalogs of datasets- you will need to explore the websites to identify and then download a specific dataset.

**Q2B: Open the data in a spreadsheet program and/or text editor. Describe what are you seeing. How can we start to make sense of this data? What documentation is available?**

**Q2C: Write a program that loads the JSON data into Python, using the workflow shown in this chapter.**
- You're welcome to explore creating a Pandas `DataFrame`, but that's not required.
- Answer to this question includes program + comments that document process and explain your code.

**Q2D: What challenges did you encounter? How did you address or solve them?**


## Question 3

**Q3A: Select another open civic dataset to use for an API call.**

You're welcome to work with the same dataset you used for Q1 or Q2 (as long as there is an API option).

But if you want to flex you API muscles, try a different open data portal to learn a new interface and data structure! Lots to choose from, but Chicago and NYC are good places to start.
- [Chicago Data Portal](https://data.cityofchicago.org/)
  * [Documentation](https://dev.socrata.com/docs/endpoints.html)
- [NYC Open Data](https://opendata.cityofnewyork.us/)
  * [Documentation](https://dev.socrata.com/docs/endpoints.html) 

Remember open data portals are catalogs of datasets- you will need to explore the websites to identify and then download a specific dataset (that has an API option).

**Q3B: What kinds of information are available in the documentation? How does that material help us start to make sense of this data?**

**Q3C: Write a program that stores the API return in Python as a Pandas `DataFrame`, using the workflows covered in this lab.**
- Answer to this question includes program + comments that document process and explain your code.

**Q3D: What challenges did you encounter? How did you address or solve them?**

## Question 4

**Q4A: Write your own Census Bureau API call.**
- You could use the same dataset as the example and modify the year, variables, geographic scope, etc.
- You could also explore other datasets.

**Q4B: What kinds of information are available in the documentation? How does that material help us start to make sense of this data?**

**Q4C: Write a program that stores the API return in Python as a Pandas `DataFrame`, using the workflows covered in this lab.**
- Answer to this question includes program + comments that document process and explain your code.

**Q4D: What challenges did you encounter? How did you address or solve them?**

## Question 5

**Q5A: Apply this workflow to another document from the [City of South Bend Document Search Center](http://docs.southbendin.gov/WebLink/Welcome.aspx?cr=1).**

- *Note- you'll need to find a document that already includes text.*

**Q5B: Briefly skim the document. What kinds of information does it contain?**

**Q5C: Write a Python program that extracts text from the document and writes the output to a `.txt` file, using the workflows covered in this lab.**

- *Answer to this question includes program + comments that document process and explain your code.*

**Q5D: Write a Python program that extracts tables from the document, and write one of these tables to a `.csv` file, using the Pandas workflow covered in this lab.**

- *Answer to this question includes program + comments that document process and explain your code.*

**Q5D: What challenges did you encounter? How did you address or solve them?**