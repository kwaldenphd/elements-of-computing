# Relational Database Terminology

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_1.png?raw=true" /></a></p>

Image from Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html).

A ***database*** is an information structure composed of identically structured records, which can be created, modified, and accessed individually…Each record of a database contains segments called fields. The set of all records sharing the same field structure is called a table. Databases structured as a single table are called flat file databases; those with multiple interlocking tables are relational databases.

As described in Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html), "Relational databases consist of one or more tables of data. These tables have fields (columns) and records (rows). Every field has a data type. Every value in the same field of each record has the same type. These tables can be linked to each other when a field in one table can be matched to a field in another table."

Linking our individual data tables in a relational database will enable us to answer the question about Puerto Rican players in Indiana without having to change the underlying data structure.

## Tables

In *Inventing the Medium*, Janet Murray describes a table as "one of the basic building blocks of information design, an extension of the list through spatialization and the bases for database design." We've worked with tabular data (i.e. data organized in a table) previously when working with CSV files.

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_1.png?raw=true" /></a></p>

Image from Library Carpentry's [Introduction to SQL tutorial](https://librarycarpentry.org/lc-sql/01-introduction/index.html).

In tabular data structures, columns headers describe the data contained in corresponding columns, or fields. Each row contains as record with data in separate column cells, or fields. These building blocks of data structured as records with fields organized in a table are the foundation of a relational database. 

Term | Definition
--- | ---
**Data** | Any collection of symbolic units, often quantitative, collected or presented for the purpose of analysis. Data becomes most useful when structured by semantic segmentation into labeled units
**Record** | An entry in a database representing a single item, made up of discrete fields
**Fields** | In a database, a field is a segment of a record with a fixed length and data type that corresponds to a single semantic unit, like a name or address
**Table** | One of the basic building blocks of information design

## Data Types

Data types commonly recognized in relational database systems include...

Type | Description | Example
--- | --- | ---
String | Used to store text or a string of non-integer characters | "This classroom is in Bond Hall" or "student"
Integer | Used to store positive or negative whole numbers | -25, 0, 25
Double | Used to store precise numerical values that include decimal points | 3.14159265359

