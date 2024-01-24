# Tidy Data Principles

Hadley Wickham's 2014 article in the *Journal of Statistical Software* outlines the foundations and principles of tidy data. These principles have become widely used in data science and other statistical software applications. 
* <em>"A huge amount of effort is spent cleaning data to get it ready for analysis, but there has been little research on how to make data cleaning as easy and effective as possible. This paper tackles a small, but important, component of data cleaning: data tidying. Tidy datasets are easy to manipulate, model and visualize, and have a specific structure: each variable is a column, each observation is a row, and each type of observational unit is a table. This framework makes it easy to tidy messy datasets because only a small set of tools are needed to deal with a wide range of un-tidy datasets. This structure also makes it easier to develop tidy tools for data analysis, tools that both input and output tidy datasets. The advantages of a consistent data structure and matching tools are demonstrated with a case study free from mundane data manipulation chores." (Hadley Wickham, Tidy Data, Vol. 59, Issue 10, Sep 2014, Journal of Statistical Software. http://www.jstatsoft.org/v59/i10.)</em>

As part of this week's work, we read Karl W. Broman and Kara H. Woo's 2018 "Data Organization in Spreadsheets" from *The American Statistician*. 
* <em>"Spreadsheets are widely used software tools for data entry, storage, analysis, and visualization. Focusing on the data entry and storage aspects, this article offers practical recommendations for organizing spreadsheet data to reduce errors and ease later analyses. The basic principles are: be consistent, write dates like YYYY-MM-DD, do not leave any cells empty, put just one thing in a cell, organize the data as a single rectangle (with subjects as rows and variables as columns, and with a single header row), create a data dictionary, do not include calculations in the raw data files, do not use font color or highlighting as data, choose good names for things, make backups, use data validation to avoid data entry errors, and save the data in plain text files." (Karl W. Broman & Kara H. Woo (2018) Data Organization in Spreadsheets, The American Statistician, 72:1, 2-10, DOI: 10.1080/00031305.2017.1375989)</em>

## What Are the Principles

Designing spreadsheets that are “tidy, consistent, and as resistant to mistakes as possible” (2)

1. Be Consistent:
  * Use consistent codes for categorical variables
  * Use a consistent fixed code for any missing values
  * Use consistent variable names
  * Use consistent subject identifiers
  * Use a consistent data layout in multiple files
  * Use consistent file names
  * Use a consistent format for all dates
  * Use consistent phrases in your notes
  * Be careful about extra spaces within cells

2. Choose Good Names for Things:
  * Avoid spaces
  * Avoid special characters
  * Be short but meaningful

3. Write Dates as YYYY-MM-DD
  * Or have separate columns for YEAR, MONTH, DATE

4. No Empty Cells

5. Put Just One Thing in a Cell

6. Make it a Rectangle
  * Single first row with variable names

7.- Create a Data Dictionary
  * “This is part of the metadata that you will want to prepare: information about the data” (6)
  * You might also find this information in a codebook that goes with a dataset
  * Things to include:
    * The exact variable name as in the data file
    * A version of the variable name that might be used in data visualizations
    * A longer explanation of what the variable means
    * The measurement units
    * Expected minimum and maximum values

8. No Calculations in the Raw Data Files

9. Do Not Use Font Color or Highlighting as Data

10. Make Backups
  * Multiple locations (OneDrive, local computer, etc.)
  * Version control program (i.e. Git)
  * Write protect the file when not entering data

11. Use Data Validation to Avoid Errors

12. Save a Copy of the Data in Plain Text Files
  * File formats can include comma-separated values (CSV) or plain-text (TXT)
  
The principles are also available as a PDF:
  * [GitHub](https://github.com/kwaldenphd/tidy-data-principles/blob/main/QualData_TidyData_Principles.pdf)
  * [Google Drive](https://drive.google.com/file/d/1lUvFePf00JfU5jMLa9zuiCcadCiFKJcR/view?usp=sharing)
  
## Common Spreadsheet Errors 

As described in Library Carpentry's ["Tidy data for librarians" tutorial](https://librarycarpentry.org/lc-spreadsheets/02-common-mistakes/index.html), common formatting problems for data in spreadsheets include:

- Multiple tables
- Multiple tabs
- Not filling in zeros
- Using bad null values
- Using formatting to convey information
- Using formatting to make the data sheet look pretty
- Placing comments or units in cells
- More than one piece of information in a cell
- Field name problems
- Special characters in data
- Inclusion of metadata in data table
- Date formatting