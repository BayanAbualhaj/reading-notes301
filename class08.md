# What I learned 


## Introduction to SQL

![SQL](https://lrdatascience.com/wp-content/uploads/2019/05/2012768_1d81_7.jpg)


**SQL** is Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database.

* popular SQL databases :
    - SQLite
    - MySQL
    - Postgres
    - Oracle
    - Microsoft SQL Server
    * All of them support the common SQL language standard, which is what this site will be teaching, but each implementation can differ in the additional features and storage types it supports.

* Relational databases(*Before SQL*):
    A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.


### select queries 101 
**we need to write SELECT statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has a specific syntax though, which is what we are going to learn in the following exercises.**

* how to select query
    1. Select query for a specific columns
        - SELECT column, another_column, …
        - FROM mytable;
    
    2. Select query for all columns
        - SELECT * 
        - FROM mytable;   
    
### Queries with constraints (Pt. 1)
**In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.**

* Select query with constraints
    - SELECT column, another_column, …
    - FROM mytable
    - WHERE condition
    - AND/OR another_condition
    - AND/OR …;

    * And below are some useful operators that you can use for numerical data 
    ![55](https://github.com/BayanAbualhaj/reading-notes301/blob/master/img/Screenshot%20(55).png?raw=true)

### Queries with constraints (Pt. 2)
**We show a few common text-data specific operators below:**
        ![56](https://github.com/BayanAbualhaj/reading-notes301/blob/master/img/Screenshot%20(56).png?raw=true)

### Filtering and sorting Query results
**Even though the data in a database may be unique, the results of any particular query may not be**

* SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
    - Select query with unique results
        * SELECT DISTINCT column, another_column, …
        * FROM mytable
        * WHERE condition(s);

    - Since the DISTINCT keyword will blindly remove duplicate rows, we will learn in a future lesson how to discard duplicates based on specific columns using grouping and the GROUP BY clause.

* Ordering results: SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause.
    - Select query with ordered results
        * SELECT column, another_column, …
        * FROM mytable
        * WHERE condition(s)
        * ORDER BY column ASC/DESC;

* Limiting results to a subset:Another clause which is commonly used with the ORDER BY clause are the LIMIT and OFFSET clauses, which are a useful optimization to indicate to the database the subset of the results you care about.
The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from. 
    - Select query with limited rows
        * SELECT column, another_column, …
        * FROM mytable
        * WHERE condition(s)
        * ORDER BY column ASC/DESC
        * LIMIT num_limit OFFSET num_offset;


### Inserting rows

* What is a Schema?the database schema is what describes the structure of each table, and the datatypes that each column of the table can contain.

This fixed structure is what allows a database to be efficient, and consistent despite storing millions or even billions of rows.

* Inserting new data:we need to use an INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert.

    - Insert statement with values for all columns
        * INSERT INTO mytable
        * VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;

    - Insert statement with specific columns
        * INSERT INTO mytable
           (column, another_column, …)
        * VALUES (value_or_expr,    another_value_or_expr, …),
        (value_or_expr_2, another_value_or_expr_2, …) …;

    - Example Insert statement with expressions
        * INSERT INTO boxoffice
        * (movie_id, rating, sales_in_millions)
        * VALUES (1, 9.9, 283742034 / 1000000);


### Updating rows 
* In addition to adding new data, a common task is to update existing data, which can be done using an UPDATE statement. Similar to the INSERT statement, you have to specify exactly which table, columns, and rows to update.

    - Update statement with values
        * UPDATE mytable
        * SET column = value_or_expr, 
            other_column = another_value_or_expr, 
           …
        * WHERE condition;
    
    - The statement works by taking multiple column/value pairs, and applying those changes to each and every row that satisfies the constraint in the WHERE clause.

### Deleting rows :
* When you need to delete data from a table in the database, you can use a DELETE statement, which describes the table to act on, and the rows of the table to delete through the WHERE clause.
    - Delete statement with condition
        * DELETE FROM mytable
        * WHERE condition;

    - if you decide to leave out the WHERE constraint, then all rows are removed, which is a quick and easy way to clear out a table completely (if intentional).
    -  Without a proper backup or test database, it is downright easy to irrevocably remove data, so always read your DELETE statements twice and execute once.


### Creating tables:
- Create table statement w/ optional table constraint and default value
    * CREATE TABLE IF NOT EXISTS mytable (
         column DataType TableConstraint DEFAULT default_value,
         another_column DataType TableConstraint DEFAULT default_value,
         …
        );

* If there already exists a table with the same name, the SQL implementation will usually throw an error, so to suppress the error and skip creating a table if one exists, you can use the IF NOT EXISTS clause.

![57](https://github.com/BayanAbualhaj/reading-notes301/blob/master/img/Screenshot%20(57).png?raw=true)


![58](https://github.com/BayanAbualhaj/reading-notes301/blob/master/img/Screenshot%20(58).png?raw=true)



### Altering tables
* SQL provides a way for you to update your corresponding tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints.

1. Adding columns
    - Altering table to add new column(s)
        * ALTER TABLE mytable
        * ADD column DataType OptionalTableConstraint 
        * DEFAULT default_value;

2. Removing columns
    - Altering table to remove column(s)
        * ALTER TABLE mytable
        * DROP column_to_be_deleted;

3. Renaming the table
    - Altering table name
        * ALTER TABLE mytable
        * RENAME TO new_table_name;

4. Other changes:Each database implementation supports different methods of altering their tables, so it's always best to consult your database docs before proceeding


### Dropping tables
* In some rare cases, you may want to remove an entire table including all of its data and metadata, and to do so, you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely

    - Drop table statement
        * DROP TABLE IF EXISTS mytable;

    - the database may throw an error if the specified table does not exist, and to suppress that error, you can use the IF EXISTS clause.
    
    - In addition, if you have another table that is dependent on columns in table you are removing (for example, with a FOREIGN KEY dependency) then you will have to either update all dependent tables first to remove the dependent rows or to remove those tables entirely.














