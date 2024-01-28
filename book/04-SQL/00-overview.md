# SQL Overview

This chapter provides an overview of basic syntax and operations in SQLite, a version of Structured Query Language (SQL). It also provides an overview of connecting relational database workflows and SQL syntax in Python.

## Acknowledgements

The author consulted the following resources when building out this chapter:
- [W3 Schools "SQL Syntax"](https://www.w3schools.com/sql/sql_syntax.asp)
- [Library Carpentry "Database Design"](https://librarycarpentry.org/lc-sql/08-database-design/index.html)
- [Library Carpentry "SQL"](https://librarycarpentry.org/lc-sql/)
- Chapter 6, "Data Loading, Storate, and File Formats" section 6.4 "Interacting With Databases" (pp. 191-193) from Wes McKinney's [*Python for Data Analysis: Data Wrangling With pandas, Numpy, and IPython*](https://www.oreilly.com/library/view/python-for-data/9781491957653/) (O'Reilly, 2017).
- David Muller, "[How To Use the `sqlite3` Module in Python 3](https://www.digitalocean.com/community/tutorials/how-to-use-the-sqlite3-module-in-python-3)" *Digital Ocean* (2 June 2020)
- Data Carpentries tutorial, "[Data Analysis and Visualization in Python for Ecologists](https://datacarpentry.org/python-ecology-lesson/09-working-with-sql/index.html)"
- Chapter 15 "Using Databases and SQL" (pp. 185-208) from Charles Severance's [*Python for Everybody: Exploring Data in Python 3*](https://www.py4e.com/) (2016).
- Nik Piepenbreier, "[Python SQLite Tutorial - The Ultimate Guide](https://towardsdatascience.com/python-sqlite-tutorial-the-ultimate-guide-fdcb8d7a4f30)", *Towards Data Science* (1 April 2020).

Peer review and editing was provided by Spring 2021 graduate teaching assistants [Aidan Draper](https://github.com/adraper2), [Eric Tsai Sahoo](https://github.com/milktea292) & [Subhadyuti Sahoo](https://github.com/SDSAHOO703).

## Chapter Table of Contents

```{tableofcontents}
```

## Data

We'll be working with a relational database file that includes the `players`, `teams`, `locations`, and `transactions` tables. Download link options are included below.
- [`data.db`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch4/data.db)
- [`data.sql`](https://raw.githubusercontent.com/kwaldenphd/elements-of-computing/main/book/data/ch4/data.sql)

## Software

Navigate to https://sqlitebrowser.org/ in a web browser. Select the download version for your operating system:
- Windows: OOP Coders, ["Install DB Browser SQLite and create database"](https://youtu.be/CDen1TavGQ8) *YouTube* (2 September 2020)
- Mac: Cool IT Help, ["Sqlite Browser Installation on Mac OS"](https://youtu.be/SkXxnasbrFY) *YouTube* (3 October 2019)
- Google Chromebook: Follow the instructions for the Debian varation of Linux. 
  * See also: Dave McKay, ["How to Use DB Browser for SQLite on Linux"](https://www.howtogeek.com/704243/how-to-use-db-browser-for-sqlite-on-linux/), *How-To Geek* (16 September 2020)

Follow the installation instructions. Once the installation is complete, launch the program.

## Application

[Click here](https://colab.research.google.com/drive/1oxQZ20oju13Peb04Jim97hGtVv0kgFMO?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

For questions that involve SQL queries, include your query in a code cell.