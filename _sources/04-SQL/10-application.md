# Application

[Click here](https://colab.research.google.com/drive/1oxQZ20oju13Peb04Jim97hGtVv0kgFMO?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

For questions that involve SQL queries, include your query in a code cell.

Q1: Write a query that gets average birth year from the `players` table, for players born after 1985. Test your query using DB Browser. Include code + comments.

Q2: Write a SQL query that returns a unique list of team names from the `teams` table, sorted in reverse alphabetical order. Test your query using DB Browser. Include code + comments.

Q3: Write an SQL query that joins the Transactions and Team_Locations tables and returns all matching columns from the Transactions table. What kind of join is this? What data does this query return? Test your query using DB Browser. Include code + comments.

Q4: Write an SQL query to return the data from the `players` table, sorted in chronological order by birth year and reverse alphabetical order by country. Test your query using DB Browser. Include code + comments.

Q5: Write an SQL query to return all data from the `players` table for players born in cities that start with the letter “S”. Test your query using DB Browser. Include code + comments.

Q6: Take at least 3 of the queries you wrote in previous sections and modify them to run within a Python environment. Include code + comments.
- For this question, your program needs to:
  * Establish a connection to the database
    * `sqlite3.connect()`
  * Create the cursor object
    * `connection.cursor()`
  * Include modified query syntax
    * `cursor.execute()`
  * Get query return and store to variable
    * `cursor.fetchall()`
  * Close connection
    * `cursor.close()`

Q7: For at least one of the Q6 queries, create a Pandas `DataFrame` from the query results and write to a `.csv` file. Include code + comments.
- For this question, your program needs to:
  * Create the dataframe
    * `pd.DataFrame()`
  * Save as CSV
    * `pd.to_csv()`