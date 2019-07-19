# SQL-Essentials-
This repository helps you get started learning SQL as a beginner. My goal is to help you understand SQL, so you can take your database skills to the next level!

# Table of Content
1. SQL Introduction
2. DDL (DATA DEFINITION LANGUAGE) COMMANDS
3. DML (DATA MANIPULATION LANGUAGE) COMMANDS
4. RETRIEVE DATA FROM MULTIPLE TABLES
5. INBUILT FUNCTIONS IN SQL
6. CREATE ADVANCE DATABASE OBJECTS

# 1. SQL Introduction
### Structured Query Language (SQL) 
Structured Query Language (SQL) is a domain-specific language used in programming and designed for managing data held in a relational database management system, or for stream processing in a relational data stream management system.

#### MySQL:
MySQL is an open-source relational database management system. Its name is combinations of “My”, the name of co-founder Michael Widenius's daughter, and "SQL", the abbreviation for Structured Query Language.

#### SQL Query:
Structured Query Language (SQL) is a standard computer language for relational database management and data manipulation. SQL is used to query, insert, update and modify data.

#### Database:
A database is an organized collection of data, generally stored and accessed electronically from a computer system.

#### RDBMS:
A relational database management system (RDBMS) is a database management system (DBMS) based on the relational model of data. Most databases in widespread use today are based on this model.

#### Schema:
A drawing that represents an idea or theory and makes it easier to understand. A database schema of a database system is its structure described in a formal language supported by the database management system.

#### Normalization:
Normalization is the process of organizing data to avoid duplication and redundancy.

##### First Normal Form	For a table to be in the First Normal Form, it should follow the following 4 rules:
1. It should only have single (atomic) valued attributes/columns.
2. Values stored in a column should be of the same domain
3. All the columns in a table should have unique names.
4. And the order in which data is stored, does not matter.

##### Second Normal Form	For a table to be in the Second Normal Form,
1. It should be in the First Normal form.
2. And, it should not have Partial Dependency.

##### Third Normal Form	A table is said to be in the Third Normal Form when,
1. It is in the Second Normal form.
2. And, it doesn't have Transitive Dependency.

##### Boyce and Codd Normal Form	A table is said to be in the Third Normal Form when,
1. It is in the Second Normal form.
2. And, it doesn't have Transitive Dependency.

##### Fourth Normal Form	A table is said to be in the Fourth Normal Form when,
1. It is in the Boyce-Codd Normal Form.
2. And, it doesn't have Multi-Valued Dependency

#### Data Types in SQL
A data type is an attribute that specifies the type of data that the object can hold: integer data, character data, monetary data, data and time data, binary strings, and so on.

##### Character String Data Type	char(n): 
Stores n characters (n bytes, where n is in the range of 1-8000)

* **nchar(n):** Stores n Unicode characters (2n bytes, where n is in the range of 1-4000)
* **varchar(n):** Stores approximately n characters (Actual string length + 2 bytes, where n is in the range of 1-8000) 
* **varchar(max):** Stores up to 231-1 characters
* **nvarchar(n):**  Stores approximately n Characters
* **nvarchar(max):** Stores up to ((231-1)/2)-2 characters

##### Numeric Data Type:
Int, tinyint, smallint, bigint, money, smallmoney, decimal(p,s), numeric(p,s), float(n), real

##### Data and Time Data Type:
Date, datatime, datetime2, datatimeoffset, smalldatatime, time

##### Binary Data Type:
Bit, binary(n), varbinary(n), varbinary(max)

##### Other Data Type:
Cursor, sql_variant, table, rowversion, uniqueidentifer, xml


# 2. DDL (DATA DEFINITION LANGUAGE) COMMANDS
DDL is short name of Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database. 
##### (a) Create 
##### (b) Alter 
##### (c) Drop

### Create Data Base Objects:
The CREATE DATABASE statement is used to create a new SQL database. 
Syntax: CREATE DATABASE <database_name>

### Create Table Statements:
The CREATE TABLE Statement is used to create table in selected database.
Syntax: CREATE TABLE <Table_Name> (ColumnA datatype, columnB datatype);

### Alter Table Statements:
**Alter table** is used to: 
(a) Add, Delete, Modify columns from existing table 
(b) Add/Drop constraints on an existing table.
**Syntax:** ALTER TABLE <table_name> ADD <column_name> <datatype>

ALTER TABLE <table_name> DROP <column_name> <datatype>

ALTER TABLE <table_name> ALTER COLUMN <column_name> <datatype>

### Drop Table Statements:
The DROP  TABLE statement is used to drop a table form selected database
Syntax: DROP TABLE <table_name>

**Various Constraints**	
* Constraints enforce rules on the table whenever row are inserted, updated and deleted from the table 
* Prevents the deletion of a table if there are dependencies from other tables
* Define the constraints at column or table level
* Constraints can be applied during creation of table or after table creation by using alter command

**NOT NULL**	Specifies that a column must have some value

**UNIQUE**	Specifies that column must have unique values

**PRIMARY KEY**	Specifies a column or a set of columns that uniquely identifies a row. It does not allow null values.

**FOREIGN KEY**	Foreign key is a column(s) that references a column(s) of a table

**CHECK	Specifies** a condition that must be satisfied by all the row in a table.

### Creating View	
A view is named, derived, virtual table. A view takes the output of a query and treats it as a table.
Syntax: CREATE VIEW <view_name> AS SELECT  * FROM <table_name>


# 3. DML (DATA MANIPULATION LANGUAGE) COMMANDS
Data Manipulation Language	Deals with data manipulation, and includes most common SQL statements, and it is used to store, modify, retrieve, delete and update data in database. '

DML Commands	This language constitutes the statements that are used to manipulate with the data. It has commands like:
#### (a) INSERT 
#### (b) UPDATE 
#### (c) DELETE 
#### (d) SELECT

#### Insert Statement:
Insert command is used to insert data/record into the database table. Inserting values for the specific columns in the table.

‘Insert-As-Select’ Statement	‘Insert-As-Select’ Statement allows to insert into a table using the input from another table. Record from one table will be inserted in another table.

#### Update Statement:
Update statement updates/modify the existing data in the tables. Using these statements we can update the value of a single column or multiple columns in a single statement. Updating single column.

#### Delete Statement:
Delete Command/Statement helps to delete rows/records from database table. Delete Statements can be executed with or without where conditions. Execution of delete commands without where condition will remove all the records/rows from the table.

#### Select Statement:
These statements help us to retrieve data or records from data table. Where condition is optional in select statement. Various operators can be used in where conditions for data retrival.

##### Distinct Value:
Value used to retrieve unique values for a column. Multiple rows can have same values for a column, distinct keyword in select statement  help us to retrieve unique row for a column

##### Ordering Result	Order By: 
Used along with where clauses to display the specified column in ascending order or descending order.  By default ascending order.

#### Filtering:
**Logical Operators (AND, OR and NOT)**	Used where condition to join more than tow queries. Used to combine the results of two or more conditions to produce single result.

**AND** : Logical Operator	Used to combine two conditions and it fetches the result which satisfy both the conditions.

**OR** : Logical Operator	OR operators is used to combine two or more conditions and it fetches the result with satisfy any one of the condition in OR statements

**NOT** : Logical Operator	NOT operator is used to negate the conditions and it fetches opposite of the result with satisfy the condition. It is used in combination with other keywords like NOT IN, NOT between etc

#### Filtering: 
**Comparison Operator  (=, !=, <>, >=, <=,  LIKE, Between, IN)**	Comparison Operators are used in where condition to fetch result from table.

**Between Operator** 	The BETWEEN operator is used to search for values that are within a set of values.

**IN Operator**	Fetches values from a set of literal. It is used to test whether or not a value is “in” the list of values provided after the keyword IN. The IN condition can be used with any data type in SQL. IN condition generally used when we want to check/fetch values from multiple values in single statement. 

**LIKE Operator**	Like condition to perform wild card searches of valid search string values
•	Search condition can contain either characters or numbers
•	% denote zero or many characters
•	_ denote one character

**Case Expression**	Used as a type of IF-THEN-ELSE Statement. Case is used to provide if-then-else type of logic to SQL


# 4. RETRIEVE DATA FROM MULTIPLE TABLES
### SQL Join:
A join clause is used to fetch data from two or more data tables, based on join condition. Join Clause is used to combine row from one (Self-Join) or more tables, based on a related column(s) between them.  
#### Self Join 	
A table can be joined to itself in a self join.
##### Syntax: 
SELECT <column_list>

FROM <table_name1> t1

JOIN<table_name1> t2

ON t1.column_name = t2.column_name;

#### Inner Join 	
The INNER JOIN fetches records that have matching values in both tables
##### Syntax:
SELECT <column_list>

FROM <table_name1> as t1

INNER JOIN<table_name2>as t2

ON t1.column_name = t2.column_name;

#### Left Outer Join	
The LEFT OUTER Join returns rows to the left (t1) even if there are no rows on the right (t2) of the join clause
The result is NULL for rows on RIGHT Table, when there is no match
##### Syntax:
SELECT <column_list>

FROM <table_name1> as t1

LEFT OUTER JOIN <table_name2> as t2

ON t1.column_name =  t2.column_name;

#### Right Outer Join	
The RIGHT OUTER Join returns rows to the right (t2) relation (table) even if there are no matching rows on the left (t1) relation table.
The result is NULL for rows on LEFT Table, when there is no match
##### Syntax:
SELECT <column_list>

FROM <table_name1> as t1

RIGHT OUTER JOIN <table_name2> as t2

ON t1.column_name =  t2.column_name;

#### Full Outer Join	
The FULL OUTER JOIN keyword return all records when there is a match in either left (t1) or right (t2) table records
If there are rows in “t1” that do not have matches in “t2” or vice-versa, those rows will be listed as well
##### Syntax:
SELECT <column_list>

FROM <table_name1> as t1

FULL OUTER JOIN <table_name2> as t2

ON t1.column_name =  t2.column_name;

#### Cross Join	
Displays all the rows and all the columns of both the tables. This is also called **Cartesian product**.
##### Syntax:
SELECT <column_list>

FROM <table_name1> as t1

CROSS JOIN <table_name2> as t2;


# 5. INBUILT FUNCTIONS IN SQL
Built-In-Functions	Built-in-Functions are used to calculate values and manipulate data. These functions can be used anywhere as expressions.
* Gets system related information
* Used for calculations
* Manipulate input data

### Conversation Functions	
Functions that support data type casting and converting.
* **CAST (expr AS datatype):** Return value of specified datatype on success Throws error on failure 
* **CONVERT (datatype, expr):** Return value of specified datatype on success Throws error on failure 
* **PARSE (value AS datatype):** Return value of specified datatype on success Throws error on failure 
* **TRY_CAST (expr AS datatype):** Returns value of specified datatype on success NULL on failure
* **TRY_CONVERT(datatype, expr):**  Returns value of specified datatype on success NULL on failure
* **TRY_PARSE (value AS datatype):** Returns value of specified datatype on success NULL on failure

### Logical Functions	
Scalar functions that perform logical operation
* **CHOOSE (index, val_1, val_2 [, val_n])** : Return a specified index from a list of values. Return NULL, if index is 0 or greater than number of items
* **IIF (boolean_expr, true_value, false_value)** : Return one of two values, based on whether the Boolean expr evaluates to true or false

### Math Functions	
Scalar functions perform a calculation, usually based on input values that are provided as arguments, and return a numeric value.
* **ABS(num_expr)** : Return absolute (positive) value of the specified numeric expr
* **RAND(seed**) : Return a pseudo-random float value from 0 to 1 (exclusive). Seed is optional value
* **EXP(float_expr)** : Returns the exponential value 
* **ROUND(num_expr, length)** : Returns a numeric value, rounded to the specified length or precision
* **FLOOR(num_expr)** : Returns the largest integer less than or equal  to the specified numeric expr
* **SIGN(num_expr)** : Returns the positive (+1), zero (0), or negative (-1) sign of the specified expr
* **SQRT(float_expr)** : Returns the square root of the specified float value
* **CEILING(num_expr)** : Returns the smallest integers greater than, or equal to, the specified numeric expr
* **SQUARE(float_expr)** : Returns the square of the specified float value
* **POWER(float_expr,y)** : Returns the value of the specified expr to the specified power

### Aggregate Functions	
Aggregate functions perform a calculation on a set of values and return a single value. Except for COUNT, aggregate functions ignore null values. Aggregate functions are frequently used with the GROUP BY clause of the SELECT Statement.
* **AVG(expr)**: Returns the average of the value in group. Null values are ignored.
* **MIN(expr)**: Returns the minimum value in the expr
* **SUM(expr)**: Returns the sum of all the values, or only the DISTINCT values, in the expr. SUM can be used with numeric columns only. NULL values are ignored.
* **COUNT()**: Returns the number of items in a group. COUNT works like the COUNT_BIG function. The only difference between the two functions is their return values. COUNT always returns an int data type values. COUNT_BIG always returns a bigint data type value.
* **MAX(expr)**: Returns the minimum value in the expr.

### String Functions	
Scalar functions perform an operation on a string input value and return a string or numeric values.
* **LTRIM (char_expr)**: Return a character expr after it removes leading blanks
* **RTRIM (char_expr)**: Returns a character string after truncating all trailing blanks
* **CHAR (int_expr)**: Covert as int ASCII code to character
* **CHARINDEX (exprToFind, exprToSearch[,start_location])**: Search an expression for another expression and returns its starting position if found
* **STR (expression)**: Returns character data converted from numeric data
* **CONCAT (str1, str2, str3..)**:  Returns a string that is the result of concatenating two or more string values
* **REPLACE (string, pattern, replacement)**: Replaces all occurrences of a specified string value with another string values
* **SUBSTRING (expr, start, length)**: Returns part of character, text
* **FORMAT value, format ([, culture])**: Returns a value formatted with the specified format and optional culture
* **LEFT (expr, int)**: Returns the LEFT part of a character string with the specified number of characters
* **RIGHT (expr, int)**: Returns the RIGHT part of a character string with the specified number of characters
* **REVERSE (string)**: Returns the reverse order of a string value
* **UPPER (string)**: Returns a character expression with lowercase character data to uppercase
* **LOWER (string)**: Returns a character expression with uppercase character data to lowercase
* **LEN (string)**: Returns the number of characters of the specified string expression, excluding trailing blanks.

### Date Functions	
Data and Time functions are scalar functions that perform an operation on a date and time input value and return either a string, numeric, or date and time value
* **SYSDATETIME()**: Returns a datetime2(7) value that contains the date and time
* **CURRENT_TIMESTAMP**:  Returns a datetime value that contains the date and time
* **DATEPART(datapart, date)**: Returns an integer that represent the specified datepart of the specified date
* **DAY(date)/MONTH(date)/YEAR(date)**: Returns an integer that represents the day/month/year part of the specified dates
* **DATEDIFF(datepart, startdate, enddate)**: Returns the number of date or time datepart boundaries that are crossed between two specified dates
* **DATEADD (datepart, number, date)**: Returns a new datetime value by adding an interval to the specified datepart of the specified date


# 6. CREATE ADVANCE DATABASE OBJECTS

