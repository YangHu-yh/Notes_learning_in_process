# INTRODUCTION

`SQL is a standard language for accessing and manipulating databases.`
	...but with some small differences between versions.

SQL can:
- execute queries
- retrieve data
- insert records
- delecte records
- create new databases
- create new tables 
- create stored procedures
- create views
- set permissions on tables, procedures, and views

### RDBMS - Relational Database Management System
- "basis for SQL and all modern database systems"
- "table is a collection of related data"

# Here it begins!

Here, we use the well-known Northwind sample database (included in MS Access and MS SQL Server) as an example, and the column (information associated with a specific field in a table) consist of CustomerID, CustomerName, ContactName, Address, City, PostalCode and Country. A record, also called a row, is each individual entry.

## Major Command

- SELECT (select all the records)
- UPDATE (updates data)
- DELETE (deletes data)
- INSERT INTO (insert new data)
- CREATE DATABASE 
- ALTER DATABASE (modifies a database)
- CREATE TABLE
- ALTER TABLE
- DROP TABLE (delects a table)
- CREATE INDEX (creates an index/search key)
- DROP INDEX (delects an index)


### SELECT
`SELECT * FROM table_names;` 
or 
`SELECT column1, column2,...
FROM table_name;`


Examples:

`SELECT CustomerID, CustomerName, City, Country
FROM Customers;`


## Something Useful!

### DISTINCT

Example:

`SELECT DISTINCT Country FROM Customers;`
`SELECT DISTINCT City FROM Customers;`

### COUNT

`SELECT COUNT(DISTINCT Country) FROM Customers;`

* `COUNT(DISTINCT column_name)` is not supported in Microsoft Access database, which is used by Firefox and Microsoft Edge in the example of w3schools.com . And MS Access need the following code:

`SELECT Count(*) AS DistinctCountries
FROM (SELECT DISTINCT Country FROM Customers); `


### WHERE 

`SELECT/UPDATE/DELETE column1, column2, ...
FROM table_name
WHERE condition;`

Example:
`SELECT * FROM Customers
WHERE Country = "France";`

`SELECT * FROM Customers
WHERE City = "London";`

or numerical/double fields

`SELECT * FROM Customers
WHERE CustomerID>=5;`

`SELECT * FROM Customers
WHERE CustomerID BETWEEN 2 AND 10;`


Operators in the WHERE Clause:

Index | Operator | Description
--- | :---:| :---
1|= | Equal
2|<>| Not equal, some versions use !=
3|>| Greater than
4|< | Less than
5|>=| Greater than or equal
6|<=| Less than or equal
7|BETWEEN| Between an **inclusive** range
8|LIKE |Search for a pattern
9|IN | To specify multiple possible values for a column 



### Notes

- SQL is not case sensitive
- `;` separate each SQL statement



# REFERENCE
- https://www.w3schools.com/sql/default.asp













