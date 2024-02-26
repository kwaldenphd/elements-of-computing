# Getting Started With Tidy Data

This chapter provides an overview of tidy data principles (Wickham et al). It covers how to recognize and address pattern errors in structured data using the data cleaning tool Open Refine and common spreadsheet programs like Microsoft Excel or Google Sheets. It also covers how to use survey design and data validation options to minimize user error in data entry.

## Acknowledgements

The author consulted the following resources when building this tutorial:
- [Library Carpentry "Tidy Data for Librarians"](https://librarycarpentry.org/lc-spreadsheets/)
- [Library Carpentry "Database Design"](https://librarycarpentry.org/lc-sql/08-database-design/index.html)
- [Library Carpentry "Open Refine"](https://librarycarpentry.org/lc-open-refine/)

## Chapter Contents

```{tableofcontents}
```

## Data

This chapter will work with two tables, verisons of the baseball data we used for relational databases and SQL. [Link to access via Google Drive](https://docs.google.com/spreadsheets/d/1YcYj_cCmdsQliYN9YNPP85pdfBD-lwa5LB9MEa7V-os/copy)
- `players`
- `teams`

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch6/drive.jpg?raw=true" width="1000"></p>

You can copy the project to your own Drive workspace, download the workbook as an `.xlsx` file, and/or download individual sheets as `.csv` files.

## Software

### Spreadsheet Programs

We'll be opening some structured data files as part of our work in this lab. You can use a spreadsheet program or text editor to access these files.

  * Text editors:
    * [TextEdit (Mac)](https://support.apple.com/guide/textedit/welcome/mac)
    * [Notepad](https://www.microsoft.com/en-us/p/windows-notepad/9msmlrh6lzf3) or [Notepad++](https://notepad-plus-plus.org/) (Windows)
    * [Atom](https://atom.io/), [Brackets](https://brackets.io/) (free download options for Mac and Windows)
    * [Text (Chromebook)](https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkjmjhdgbg?hl=en)  
  * Spreadsheet programs:
    * [Microsoft Excel (Windows or Mac)](https://nd.service-now.com/nd_portal?id=kb_article&sys_id=cf15b58edbaa3058310fa94ed3961935)
      * ND students have free access to the Microsoft Office suite through Office365
    * [Apple Numbers (Mac)](https://www.apple.com/numbers/)
    * [LibreCalc (open source Excel/Numbers alternative for Mac or Windows users)](https://www.libreoffice.org/download/download/)
    * [Google Sheets (web-based option available through Google Drive)](https://www.google.com/sheets/about/)


### OpenRefine

We'll also be working with a free software program called OpenRefine as part of our work in this lab. 

Navigate to https://openrefine.org/download.html in a web browser and download the appropriate version for your operating system.
- If you are getting memory-related error messages, visit https://docs.openrefine.org/manual/installing#increasing-memory-allocation to troubleshoot.

## Application

[Click here](https://docs.google.com/document/d/1zRGhTwuTrj0hUpLZABRg1w7JPznE0hE06wo1414lng8/copy) for a Google Doc template for this chapter's application problems.

To include screenshots in your doc:
- [Tutorial for adding images/tables/drawings to a Google Doc](https://www.techrepublic.com/article/how-to-add-images-tables-and-drawings-to-a-google-doc-file/)
  * Windows ([Snipping Tool](https://support.microsoft.com/en-us/windows/use-snipping-tool-to-capture-screenshots-00246869-1843-655f-f220-97299b865f6b) for folks running older versions of Windows; [Snip & Sketch](https://www.lifewire.com/snip-and-sketch-windows-10-4774799) for folks running updated versions)
  * [Mac](https://support.apple.com/en-us/HT201361)
  * [Google Chromebook](https://support.google.com/chromebook/answer/10474268?hl=en)

We'll also use a combined spreadsheet template for the data cleaning outputs.

[Click here](https://docs.google.com/spreadsheets/d/1n6oDPMh3G7dLTzLdMcr6oFepovilONg8v-3XQC3r6ag/copy) to make a copy of the Google Sheets template.
- [Tutorial for importing CSV files into Google Sheets](https://help.loyverse.com/help/how-open-csv-file-google-sheets)