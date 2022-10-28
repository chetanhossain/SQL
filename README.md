SQL Transcription

To run any business (small or large scale), the most essential requirement is data. Without data, there is no business. 
DATA: A collection of raw facts that have no meaning
INFORMATION: Processed data that have a meaning

EX: This chetan is: this is data. This is a collection of data that isn't processed and therefore has no meaning.
This is Chetan: this is information. The data has been processed and output into something that has a meaning

Why is this important? 
When we are inputting something into a computerm it is intput as data. Inside the computer there are a lot of different kinds of processes that manupulate the data so that the output becomes information/

We store data specifically in a database. (NOTE: remember that computers cannot automatically store data. Users need to store data in a database). However, the user cant simply tell the computer to store data and it would happen just like that. This is where database management systems come into play. Database management systems (DBMS) allow the user to access and manipulate the database. The way we communicate to the DBMS to help us manipulate the data is by utilizing a language we call SQL
Fun fact: Before we had computers, data in businesses were stored in physical files. In order to manipulate those files you needed a file management system or FMS.

A Brief History of SQL
1970 − Dr. Edgar F. "Ted" Codd of IBM is known as the father of relational databases. He described a relational model for databases.
1974 − Structured Query Language appeared.
1978 − IBM worked to develop Codd's ideas and released a product named System/R.
1986 − IBM developed the first prototype of relational database and standardized by ANSI. The first relational database was released by Relational Software which later came to be known as Oracle.


There are multiple kinds of DBMS
NDBMS: Network database management system
HDBMS: Heirarchal database management system 
ODBMS: Object oriented database management system
RDBMS: Relational database management system 

Currently the most popular type of DBMS (and the one we will be covering in this tutorial) currently being used right now is RDBMS. In a relational database management system, data is stored in tables. Some examples of widely used RDBMS would be Oracle, Microsoft SQL Server, and MYSQL.

RELATIONAL VS NONRELATIONAL DATABASES:
A relational database is the database management system in which data is stored in distinct tables from where they can be accessed or reassembled in different ways, whereas a Non-Relational Database is a database architecture that is not built around tables.

Different kinds of SQL Dialects

-PL/SQL stands for procedural language/SQL. It is developed by Oracle for the Oracle Database.
-Transact-SQL or T-SQL is developed by Microsoft for Microsoft SQL Server.
-PL/pgSQL stands for Procedural Language/PostgreSQL that consists of SQL dialect and extensions implemented in PostgreSQL
-MySQL has its own procedural language since version 5. Note that MySQL was acquired by Oracle.


What is SQL?
SQL: Stands for structured query language. It allows a user to communicate to an DBMS to have it perform actions on a database. SQL is made up of various sublanguages 
DDL: Data definition language (accounts for create, alter, drop, truncate commands)
DML: Data manipulation language (accounts for insert, update, and delete commands)
DRL: Data retrieval language (accounts for select command)
DCL: Data control language (accounts for grant and revoke commands)
TCL: Transaction control language (accounts for commit, rollback, and sewpoint commands)

SOME OF THE THINGS SQL CAN DO
-execute queries against a database
-retrieve data from a database
-insert records in a database
-update records in a database
-delete records from a database
-create new databases
-create new tables in a database
-create stored procedures in a database
-create views in a database
-set permissions on tables, procedures, and views

NOTE: 
Acronym to know what DDL does
D
Rop 
Create
Alter
Truncate

Acronym for DML
Update
Insert
Delete

Understanding tables
The top of the table that defines what each column will have is called the header or definition of the table. The bottom part of the table is referred to data. In order to create and define the table, we needed to use DDL. In order to populate the table with data, we used data DML. Now whenever we want to look at the contents of the table, we would use DRL.

What is a field?
A field is a column in a table that is designed to maintain specific information about every record in the table.

What is a record?
A record is also called as a row of data is each individual entry that exists in a table

What is a column?
A column is a vertical entity in a table that contains all information associated with a specific field in a table.

What is a NULL value?
A NULL value in a table is a value in a field that appears to be blank, which means a field with a NULL value is a field with no value. It is very important to understand that a NULL value is different than a zero value or a field that contains spaces. A field with a NULL value is the one that has been left blank.

What are SQL Constraints?
Constraints are the rules enforced on data columns on a table. These are used to limit the type of data that can go into a table. Constraints can either be column level or table level. Column level constraints are applied only to one column whereas, table level constraints are applied to the entire table.

COMMON CONSTRAINTS:
NOT NULL Constraint − Ensures that a column cannot have a NULL value.
DEFAULT Constraint − Provides a default value for a column when none is specified.
UNIQUE Constraint − Ensures that all the values in a column are different.
PRIMARY Key − Uniquely identifies each row/record in a database table.
FOREIGN Key − Uniquely identifies a row/record in any another database table.
CHECK Constraint − The CHECK constraint ensures that all values in a column satisfy certain conditions.
INDEX − Used to create and retrieve data from the database very quickly.

Data Integrity
WHAT IS DATA INTEGRITY?
Data Integrity is ensuring that the logical and physical data stored in SQL Server are structurally sound and consistent. It means that the data present in SQL Server is written correctly and is where it is expected to be.

The following categories of data integrity exist with each RDBMS −
Entity Integrity − There are no duplicate rows in a table.
Domain Integrity − Enforces valid entries for a given column by restricting the type, the format, or the range of values.
Referential integrity − Rows cannot be deleted, which are used by other records.
User-Defined Integrity − Enforces some specific business rules that do not fall into entity, domain or referential integrity.

What is an Operator in SQL?

An operator is a reserved word or a character used primarily in an SQL statement's WHERE clause to perform operation(s), such as comparisons and arithmetic operations. These Operators are used to specify conditions in an SQL statement and to serve as conjunctions for multiple conditions in a statement.
-Arithmetic operators
-Comparison operators
-Logical operators
-Operators used to negate conditions


How does Data control language(DCL) work?
DCL has to do more with granting and taking away access to the data. Granting and revoking a users ability to read and write data

Create: When youre creating a table you want to specify the name of the table and also specify and define all of the columns in the table.
EX: CREATE table student (id int, name char(10))
What we are doing here is that were creating a table called student. In that table we are gonna have 2 columns, 1 will be named id and one will be named name. The only type of data that will be accepted in the id column is intergers and the only type of data that will be accepted in name would be string of char up to a total of 10

ALTER: We use alter to modify the tables. There are 4 main ways we can alter a table.
1. We can add a new column to an existing table
EX: ALTER table Student ADD Last_name char(20). The output of this is that there will be a new column in the student table and its named Last_name and it will only accept strings that are up to 20 characters long as data
2. We can drop existing tables 
EX: ALTER table Student DROP column Last_name. The output of this is that the column titled Last_name will be removed feom the table alongside all of the data inside it.
3.You can modify the type of data thats accepted by each column. 
EX: ALTER table Student ALTER column name varchar(10). The output of this is that now the only type of data that the name column will accept is varchar with a maximum string size of 20 characters
4. You can alter the size of the data accepted.
EX: ALTER table Student ALTER column char (5). The output to this is that the name column will only accept string size of a maximum of 5 characters

DROP: Dropping is when youre permanenetly delete something from the database
Ex: DROP table Student. This will delete the entire student table from the database.

Truncate: Truncate will remove all of the data inside a table. The header will still remain.

INSERT: Insert data into a table 
EX: Insert into Student values (1, "Smith")
Because the student table has 2 rows, the first row being the ID column and the second column being the name column. When inserting data into a database, you have to make sure the order that you insert your data matches the order of the columns in the table. NOTE: you also dont need to make multiple insert commands if you need to add multiple records of data
EX: INSERT into Student values (1, "Smith"), (2, "Ross"), (3, "Charlie)

What happens when you dont have the data for each column but wish to insert partial data?
If you were to do INSERT into Student values (4) because you dont know the name of the 4th user. If you were to run this, you would get an exception. In order to add specific values to sepecific columns you have to define what columnns you want to add data into in your query
EX: INSERT into Student(id) values (4). This way the id column will have 4 in it and the name column will have the value NULL

Update: Update data in a table
Following the last action we did, lets say that we wanted to update the name column where the id is 4. You would write the following query
UPDATE table Student set name = "Paddy" WHERE id = 4. Now when you look at the record with the user id of 4, youll see that the name Paddy exists there.

DELETE: Remove data
Delete will permanently remove data from the table.
EX: DELETE from Student where ID = 4. The output of this is paddy and id 4 will be removed from the table. 

What is the difference between Truncate and Delete? (Common interview question) 
1. Delete is a DML command where Truncate is a DDL command. 
2. You can specify what you want to DELETE using clauses like WHERE and HAVING. You cannot specify what you want to truncate.
3. When youre deleting data youre just removing data from the table. When youre truncating a table youre deleting the entire table and then recreating it without the data, just the headers.

UNDERSTANDING .MDF and .LDF
When creating a database, 2 files are created. A .MDF (master data file) and a .LDF (log data file). Inside the .mdf contains something called extents. Each extent is a set of 8 pages of data all having a maximum capacity of 8kb. So an extent has a total data capacity of 64KB. When adding data to a database, the data gets stored in each page of the extents in the .mdf file. 

When youre deleting data, you are taking data out of the .mdf file and putting it in the .ldf file. When youre truncating something, youre just deleting the table and recreating it in the database, so because of that, truncate is faster than delete.

SQL ALIASES
SQL alias allows you to assign a table or a column a temporary name during the execution of a query. SQL has two types of aliases: table and column aliases.
SQL Column Aliases: One of the ways you can do this is by using the AS keyword. You specify which column you want to change followed by the AS keyword followed by the name that you wish to temporarily assign

More SQL COMMANDS
- SELECT - extracts data from a database
- CREATE INDEX - creates an index (search key)
- DROP INDEX - deletes an index
- SELECT DISTINCT - return only distinct (different) values.
- WHERE - A clause that helps filter through records. 

UNDERSTANDING SQL SYNTAX

Like a natural language, SQL starts with whatever action you want to make (SELECT, DELETE, INSERT, ETC), followed by the subject and predicate 
LITERALS: Literals are explicit values which are also known as constants. In SQL there’s three kinds of literals: string, numeric, and binary.
IDENTIFIERS: dentifiers refer to specific objects in the database such as tables, columns, indexes, etc. SQL is case-insensitive with respect to keywords and identifiers.
COMMENTING: To document SQL statements, you use the SQL comments. When parsing SQL statements with comments, the database engine ignores the characters in the comments. (Use the double dash “—“)

JOINS:
Here are the different types of the JOINs in SQL:
* (INNER) JOIN: Returns records that have matching values in both tables
* LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
* RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
* FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table
