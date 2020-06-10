# SQL

### We retrieve data from SQL databases by writing a SELECT statement (which is a query).

##### A table is a type of entity, a row is an instance of that entity, and a column is a common property shared amongst entity instances.

##### Example: SELECT column, another_column,
##### FROM mytable;

##### SELECT * selects all columns in a table

### Queries with constraints

##### To filer certain results form being returned, one must use a WHERE clause in their query.

##### Example: SELECt column, another_column,
##### FROM mytable
##### WHERE condition
#####    AND/OR another_condition
#####    AND/OR ...;

##### Complex clauses can be constructed by joining numerous AND or OR logical keywords (such as num_wheels >= 4 AND doors <=2>).

##### Examples: =, !=, <, <=, >, >= are standard numerical operators. In SQL, they are col_name ! 4, for example.

##### BETWEEN...AND. Number is within range of two values (inclusive). In SQL, it's col_name BETWEEN 1.5 AND 10.5.

##### writing clauses to constrain the set of rows returned also allows the query to run faster due to the reduction in unnecessary data being returned.

##### = is a condition that is case sensitive exact string comparison.

##### != or <> is a condition that is case sensitive exact string inequality comparison.

##### LIKE is a condition that is case insensitive exact string comparison.

##### NOT LIKE is a condiiton case insensitive exact string inequality comparison.

##### % is a condition that is used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)

##### - is used anywhere in a string to match a single character (only with LIKE or NOT LIKE)

##### IN is a condition where string exists in a list

##### NOT IN is a condition where string does not exist in a list.

### Filtering and sorting Query results

##### SQL provides a convenient way to discard rows that have a duplicate column value byy using the DISTINCT keyword.

##### Example: SELECT DISTINCT column, another_column
##### FROM mytable
##### WHERE conditions(s)

##### most data in real databases are added in no particular column order. As a result, it can be difficult to read through and understand the results of a query as the size of a table increases to thousands or even millions rows.

##### SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause.

##### SELECT column, another_column,
##### FROM mytable