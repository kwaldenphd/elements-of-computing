# Using OpenRefine

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/tidy-data-principles/blob/main/figures/Figure_3.png?raw=true" alt="Capture_2"  /></p>

As described in Library Carpentry's ["Introduction to OpenRefine"](https://librarycarpentry.org/lc-open-refine/01-introduction/index.html):

<blockquote>
<p>"OpenRefine displays data in a tabular format. Each row will usually represent a ‘record’ in the data, while each column represents a type of information. This is very similar to how you might view data in a spreadsheet or database. As with a spreadsheet, the individual bits of data live in ‘cells’ at the intersection of a row and a column.</p>
<br>
<p>OpenRefine only displays a limited number of rows of data at one time. You can adjust the number choosing between 5, 10 (the default), 25 and 50 at the top left of the table of data. You can navigate through the records by using the previous/next/first/last navigation options at the top right of the table of data."</p></blockquote>

## Faceting and Filtering

As described in Library Carpentry's ["Introduction to OpenRefine"](https://librarycarpentry.org/lc-open-refine/01-introduction/index.html):

<blockquote><p>"Facets are one of the most useful features of OpenRefine and can help in both getting an overview of the data and to improve the consistency of the data.</p>
<br>
<p>A ‘Facet’ groups all the values that appear in a column, and then allows you to filter the data by these values and edit values across many records at the same time.</p>
<br>
<p>The simplest type of Facet is called a ‘Text facet’. This simply groups all the text values in a column and lists each value with the number of records it appears in. The facet information always appears in the left hand panel in the OpenRefine interface.</p>
<br>
<p>To create a Text Facet for a column, click on the drop down menu at the top of the publisher column and choose `Facet -> Text Facet`. The facet will then appear in the left hand panel.</p>
<br>
<p>The facet consists of a list of values used in the data. You can filter the data displayed by clicking on one of these headings.</p>
<br>
<p>You can include multiple values from the facet in a filter at one time by using the `Include` option which appears when you put your mouse over a value in the Facet.</p>
<br>
<p>You can also invert the filter to show all records which do not match your selected values. This option appears at the top of the Facet panel when you select a value from the facet to apply as a filter."</p></blockquote>

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/tidy-data-principles/blob/main/figures/Figure_4.png?raw=true" alt="Capture_2"  /></p>

Select the drop-down arrow for one of the columns that contains a pattern error. Select `Facet > Text Facet`. 

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/tidy-data-principles/blob/main/figures/Figure_5.png?raw=true" alt="Capture_2"  /></p>

The facet will now appear on the left-hand side of the page. Click a line in the facet to select rows with that value.
- Use the `Include` option to select multiple values.
- Use the `Edit` option to address a pattern error.

Do this for other pattern errors. Consult the following resources as needed to understand this data:
- [ISO 3166 country code table (Wikipedia)](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Decoding_table)
- [United Nations geographic regions](https://unstats.un.org/unsd/methodology/m49/)
- [USPS list of state abbreviations](https://about.usps.com/who-we-are/postal-history/state-abbreviations.htm)
- [Wikipedia list of baseball team abbreviations](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_Baseball/Team_abbreviations)
- [Wikipedia glossary of baseball jargon](https://en.wiktionary.org/wiki/Appendix:Glossary_of_baseball)

## Exporting from OpenRefine

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/tidy-data-principles/blob/main/figures/Figure_6.png?raw=true" alt="Capture_2"  /></p>

Click on the `Export` button in the top right-hand corner and select the option to export your OpenRefine project as a CSV file. 

<blockquote>NOTE: OpenRefine will only export the rows of data selected in your current review. Be sure to remove all filters or facets before exporting.</blockquote>

Make sure this file has a unique name and is saved in a location where you can find it again. Open this new CSV file in a spreadsheet program. Check to see the pattern errors have been addressed.

## Application

Q2A: Starting with the pattern errors you identified for Q1, how would you address those issues using OpenRefine?

Q2B: Provide an outline for your data processing workflow. A set of steps or tasks is a good place to start. You're welcome to include screenshots as that would be helpful.

Q2C: Work through cleaning the `players` and `teams` tables. Once you're done, export the `.csv` files and add them to the Google Sheets template for this chapter.

Q2D: Compare your experience working in OpenRefine to other experiences you have had in a text editor or spreadsheet program. In what ways do you understand, perceive, or relate to the data differently through working in OpenRefine? Reflect on and describe your experience cleaning this data in OpenRefine.

## Additional Resources

We are barely scratching the surface of what is possible with data wrangling in OpenRefine. The progam can also standardize capitalization, remove leading and trailing spaces, and address other commonly-found data errors. [Library Carpentry's OpenRefine tutorial](https://librarycarpentry.org/lc-open-refine/) goes in to greater detail about many of these other functions.