# Getting Started With SQL 

Now that we have a foundational understanding of relational database structures, we'll learn how we interact with a database using a version of a structured query language (SQL).

## SQL Overview

SQL stands for Structured Query Language. SQL "is a domain-specific language used in programming and designed for managing data held in a relational database management system (RDBMS)...It is particularly useful in handling structured data, i.e. data incorporating relations among entities and variables" ([Wikipedia, "SQL"](https://en.wikipedia.org/wiki/SQL)).

SQL was developed by IBM in the early 1970s. Relational Software, Inc. (now Oracle Corporation) released the first commercial implementations of SQL in the late 1970s. The American National Standards Institute (ANSI) and the International Organization for Standardization (ISO) adopted SQL as the official database query language in 1986. SQL is maintained by the ISO and is updated semi-regularly (typically every three years).
- [Link to official SQL documentation](https://standards.iso.org/ittf/PubliclyAvailableStandards/index.html)

For more on SQL history:
- Codd, Edgar F. (June 1970). "A Relational Model of Data for Large Shared Data Banks". *Communications of the ACM.* 13 (6): 377–87. https://doi.org/10.1145%2F362384.362685
- Chamberlin, Donald (2012). "Early History of SQL". *IEEE Annals of the History of Computing.* 34 (4): 78–82. https://doi.org/10.1109%2FMAHC.2012.61
- Chamberlin, Donald D; Boyce, Raymond F (1974). "SEQUEL: A Structured English Query Language." *Proceedings of the 1974 ACM SIGFIDET Workshop on Data Description, Access and Control. Association for Computing Machinery*: 249–64. https://doi.org/10.1145/800296.811515

### SQLite

We'll be using an implementation of SQL known as SQLite. "SQLite is a C-language library that implements a small, fast, self-contained, high-reliability, full-featured, SQL database engine. SQLite is the most used database engine in the world. SQLite is built into all mobile phones and most computers and comes bundled inside countless other applications that people use every day" ([SQLite, "What Is SQLite?"](https://www.sqlite.org/index.html)).

SQLite drives many commonly used programs and applications, including:
- Chrome, Firefox, and Safari web browsers
- Django
- Drupal
- Ruby on Rails
- Adobe Systems
- Evernote
- Skype
- iPhone text messages

Taking a quick look at SQLite's [Download](https://www.sqlite.org/download.html) and [Documentation](https://www.sqlite.org/docs.html) pages would suggest setting up a full implementation of STLite in your local computer environment is a tall order.
- *All hail the work of compilers*

We're going to use a graphical-user interface (GUI) browser application that runs on top of SQLite. [Database Browser for SQLite (DB Browser)](https://sqlitebrowser.org/) is an open-source application that provides a graphical user interface for connecting to and interacting with a SQLite database. The DB Browser application bundles SQLite, so you won’t need to install SQLite separately.

## Creating A Database

There are multiple workflows for creating a database from scratch, including using SQL's `CREATE TABLE` and `INSERT` commands. We can also import individual `.csv` files and set up the key relationships manually.

If you end up wanting or needing to create a relational database from scratch, Prof. Walden is happy to share additional resources.

But for our purposes, we'll start with a relational database file that includes the `players`, `teams`, `locations`, and `transactions` tables. Google Drive access links are included below.
- [`data.db`](https://drive.google.com/file/d/1x7pQc6Q44FNqPwysrHRWms4hni4rxZOH/view?usp=sharing)
- [`data.sql`](https://drive.google.com/file/d/1seqKJRecxNC4DxqoWZmsHxvheGtLNDYn/view?usp=sharing)

### Foreign Key Settings

Before we open our database file, we have to change a foreign key constraint within the DB Browser application.

<p align="center"><a href="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_4.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_4.png?raw=true" /></a></p>

Select the `Edit Pragmas` tab.

<p align="center"><a href="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_7.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_7.png?raw=true" /></a></p>

Uncheck the box next to `Foreign Keys`. Click `Save`. 

We can now load the sample database file.

### Loading Our Data

<p align="center"><a href="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/sqlite-intro/blob/main/screenshots/Figure_1.png?raw=true" /></a></p>

You should now be seeing the GUI (graphical user interface) window for the DB Browser application. Click the `Open Database` icon in the top-left hand menu bar, or select `Open Database` under `Files`. 

Load the `data.db` or `data.sql` file.

Save this database with a `.db` file extension in a dedicated location on your computer.