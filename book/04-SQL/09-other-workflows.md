# Other Data Workflows

There are lots of different ways to build on the relational database concepts we've covered.

## Other Relational Database Workflows

<p align="center"><img class="aligncenter" src="https://www.mobulous.com/blog/wp-content/uploads/The-Top-15-Databases-For-Web-Apps-1024x342.png" /></a></p>

Examples of relational database platforms include `MySQL`, `Oracle`, `MariaDB`, and `MongoDB`.

### Cloud Database Workflows 

In most enterprise systems, database access is managed through cloud or web-based systems.

Examples include `Microsoft Azure` or `Google Cloud`. 

For example, Notre Dame's data repository (`DataND`) uses Amazon Web Services for storage and provides user access via[AWS Snowball](https://aws.amazon.com/snowball/).

## NoSQL Workflows 

<p align="center"><img class="aligncenter" src="https://miro.medium.com/v2/resize:fit:1188/1*S54DlHzclu69JqGLgM4xyA.jpeg" /></a></p>

Non-SQL (NoSQL) databases are a robust data storage option that is not based on table relationships. Examples of NoSQL workflows can include a variety of different data structures.

### Graph Object  

<p align="center"><img class="aligncenter" src="https://phoenixnap.com/kb/wp-content/uploads/2021/04/Graph-vs-Relatioanal-visually.png" /></a></p>

For example, a graph (or graph object) database uses nodes and relationships to store data. 

### Additional Resources

For more on SQL versus NoSQL workflows:
- "[SQL vs. NoSQL Database: When to Use, How to Choose](https://www.ml4devs.com/articles/datastore-choices-sql-vs-nosql-database/)" *ML4Devs blog post* (7 July 2021)

## Alternate File Formats

Especially when working with large datasets, `.csv` files can be prohibitely resource intensive for processing, runtime, memory, etc.

<p align="center"><img class="aligncenter" src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*QEQJjtnDb3JQ2xqhzARZZw.png" /></a></p>

Alternate data structures that incorporate column-based (rather than row-based) data storage have emerged as alternatives. 

<p align="center"><img class="aligncenter" src="https://www.dremio.com/wp-content/uploads/2022/04/chart-1024x412.png" /></a></p>

Specific file formats include `Parquet` and `Feather`. We will not be covering these workflows in depth, but some resources that can get folks started:

<iframe width="560" height="315" src="https://www.youtube.com/embed/u00hCcpY6ng?si=tNmKpwWuTbJNKjD3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/9LYYOdIwQXg?si=ePD8qXfqESpnUwCX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Other resources:
- tomaztsql, “[Comparing performances of CSV to RDS, Parquet, and Feather file formats in R](https://www.r-bloggers.com/2022/05/comparing-performances-of-csv-to-rds-parquet-and-feather-file-formats-in-r/)” *R-bloggers* (8 May 2022)
- Databricks, “[Parquet](https://www.databricks.com/glossary/what-is-parquet)” *Databricks.com*
- [Apache Parquet website/documentation](https://parquet.apache.org/)
- Hadley Wickham, “[Feather: A Fast On-Disk Format for Data Frames for R and Python, powered by Apache Arrow](https://posit.co/blog/feather/)” *Posit blog* (29 May 2016)
- Feather website/documentation
  * [RStudio](https://github.com/wesm/feather)
  * [Python](https://arrow.apache.org/docs/python/feather.html)

