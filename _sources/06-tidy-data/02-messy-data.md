# Dealing With Messy Data

This chapter will work with two tables, verisons of the baseball data we used for relational databases and SQL. [Link to access via Google Drive](https://docs.google.com/spreadsheets/d/1YcYj_cCmdsQliYN9YNPP85pdfBD-lwa5LB9MEa7V-os/copy)
- `players`
- `teams`

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/drive.jpg?raw=true" width="1000"></p>

You can copy the project to your own Drive workspace, download the workbook as an `.xlsx` file, and/or download individual sheets as `.csv` files.

Explore the tables tables (sheets/tabs in the combined workbook or separate `.csv` files), thinking about the types of information included or represented in different tables and fields.

## Identify Patterns and Brainstorm Solutions

Compare what you see in these tables to tidy data principles. Start by looking for small-scale discrepencies and inconsistencies within the datasets.

You may need to consult the following resources as needed to understand this data:
- [ISO 3166 country code table (Wikipedia)](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Decoding_table)
- [United Nations geographic regions](https://unstats.un.org/unsd/methodology/m49/)
- [USPS list of state abbreviations](https://about.usps.com/who-we-are/postal-history/state-abbreviations.htm)
- [Wikipedia list of baseball team abbreviations](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_Baseball/Team_abbreviations)
- [Wikipedia glossary of baseball jargon](https://en.wiktionary.org/wiki/Appendix:Glossary_of_baseball)

## Application

Q1A: Provide three (3) distinct examples from the sample datasets (either table) that do not conform to tidy data principles. Include the example as well as an explanation of how this example does not conform to tidy data principles.

Q1B: Take a step back and consider the pattern errors you're seeing in these datasets. What trends do you notice? Any thoughts or ideas as to how or why these pattern errors might have occurred?

Q1C: How would you address these pattern errors so the data conforms to tidy data principles? Explain what steps you would take to address at least 3 pattern errors. Each error explanation should include three parts:
- An example of the issue
- An explanation of your method to address the issue 
- The same example as tidy data