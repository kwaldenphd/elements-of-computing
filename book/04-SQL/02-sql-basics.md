# Basic Syntax

What is SQL? As described in Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html), "Structured Query Language, or SQL (sometimes pronounced 'sequel'), is a powerful language used to interrogate and manipulate relational databases. It is not a general programming language that you can use to write an entire program."

When working with relational database systems, we can use SQL to write queries. As described in Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html), "a query is a question or request for data. For example, “How many journals does our library subscribe to?” When we query a database, we can ask the same question using a common language called Structured Query Language or SQL in what is called a statement. Some of the most useful queries - the ones we are introducing in this first section - are used to return results from a table that match specific criteria."

## DB Browser Setup

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_4.jpg?raw=true" /></p>

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_5.jpg?raw=true" /></p>

In the DB Browser program, select the `Open Database` icon. Open the `.db` file from the previous section.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_6.jpg?raw=true" /></p>

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_7.jpg?raw=true" /></p>

Click the `Execute SQL` tab. The top text-box on the left-hand pane in the program (immediately below `SQL 1`) is where we will type SQL statements.

<p align="center"><img class=" size-full wp-image-55 aligncenter" src="https://github.com/kwaldenphd/sql-queries-joins/blob/main/screenshots/Figure_8.jpg?raw=true" /></p>

Once we start adding SQL syntax, we can run all (or a selection) using the single arrow icon (left of the two arrows, immediate right of print). 
- We can use the other arrow (right of the two arrows) to run a single line.

## Comments

We can add single-line comments to our SQL statements using a double dash `--`.

```SQL
-- this is my single-line comment
```

## Section Table of Contents

```{tableofcontents}
```