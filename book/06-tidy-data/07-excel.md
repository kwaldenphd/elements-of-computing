# Microsoft Excel

## Loading Data

There are two options for loading data files in Excel.
  * Import CSV files
  * Open Excel workbook

### Loading Data From CSV Files

Open a blank Microsoft Excel file. Save the blank file as an Excel workbook.

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig7.png?raw=true" width="1000"></p>

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig8.jpg?raw=true" width="1000"></p>

Click on `Data` in the top menu bar. Under `Get Data` select the `From Text/CSV` option. In `Sheet1`, select the `Player_Birthplaces.csv` file.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig9.jpg?raw=true"/></p>

In the pop-up window, make sure `Comma` is selected as the delimiter, and switch `File Origin` to `UTF-8`. Click `Load`

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig10.png?raw=true"/></p>

You should now see the CSV data in the Excel workbook. Go through the same process for the `team_locations.csv` file. Save the updated workbook.

### Loading Data as an Excel Workbook

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig11.jpg?raw=true" width="1000"></p>

Alternatively, you can download the Google Sheets file as an Excel workbook (`.xlsx`). That workbook file includes both tables needed for this lab.

## Data Cleaning in Excel

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig12.png?raw=true" width="1000"></p>

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig13.jpg?raw=true" width="1000"></p>
 
Click the drop-down arrow next to a column header to see additional options for that field. Use these sort, search, and filter options to address data pattern errors.

### Find and Replace

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig14.png?raw=true" width="1000"></p>

Alternatively, use the `Replace` option under `Find & Select` (in the `Home` menu section) to address pattern errors.

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig15.jpg?raw=true" width="1000"></p>

Click the `Options` button to see additional options.
 
Consult the following resources as needed to understand this data:
- [ISO 3166 country code table (Wikipedia)](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Decoding_table)
- [United Nations geographic regions](https://unstats.un.org/unsd/methodology/m49/)
- [USPS list of state abbreviations](https://about.usps.com/who-we-are/postal-history/state-abbreviations.htm)
- [Wikipedia list of baseball team abbreviations](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_Baseball/Team_abbreviations)
- [Wikipedia glossary of baseball jargon](https://en.wiktionary.org/wiki/Appendix:Glossary_of_baseball)

<blockquote>To change all cells in a column, click the cell in the first non-header row. Press <code>Control</code> or <code>Command</code> and the down arrow key to select all cells with data in that column. Press <code>Control/Command</code> and <code>D</code> to copy the first value into the other selected cells. Alternatively, move your cursor over the bottom right-hand corner of the cell in the first non-header row. Click and drag the plus icon that appears down through the column to copy the value in the first cell into the subsequent cells.</blockquote>

Go through this same process for the `teams` table.

## Saving and Exporting in Excel

The default file type in Microsoft Excel is an Excel workbook (`.xlsx`).

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/fig16.png?raw=true" width="1000"></p>

Click on the `File` menu section to show additional export options. Under `Export` you can see some of the other options for exporting the data in Excel.
  * While plain-text formats (tab separated values, `tsv`; comma separated values, `csv`, etc) are best for digital preservation and interoperability, they only accept a single table.

## Application

Q3A: Starting with the pattern errors you identified for Q1, how would you address those issues using Excel?

Q3B: Provide an outline for your data processing workflow. A set of steps or tasks is a good place to start. You're welcome to include screenshots as that would be helpful.

Q3C: Work through cleaning the `players` and `teams` tables. Once you're done, export the `.csv` files and add them to the Google Sheets template for this chapter.

Q3D: Compare your experience working in a spreadsheet program to other experiences you have had in a text editor, spreadsheet program, or OpenRefine. In what ways do you understand, perceive, or relate to the data differently through working in a spreadsheet program? Reflect on and describe your experience cleaning this data in a spreadsheet program.