tags : #introductionToSQL 

#### Introduction : 

Structured Query Language is set of commands used to operate on relational databases. Although we refer to SQL as query language, it can do much more than just querying the database. It can define structure of data, modify data in database and specify security constraints.

#### What is a *query language* ?

A query language is language is a language in which a user requests information from the database. This languages are on a level higher than that of standard programming language. Query languages can be categorized as either *procedural* or *non procedural*. 

In procedural query language, the user instructs a system to perform a sequence of operations on the database to compute the desired result.

In non-procedural language, the user describes the desired information without giving a specific procedure for obtaining that information.

Query languages used in practice includes elements of both procedural and non-procedural
languages. The relational algebra consists of operations that takes two or more relations as input and produces one relation as output according to conditions provided. SQL supports relational algebra so user can combine two or more relations and analyze data in resultant relation. 

#### Brief history : 

IBM developed the original version of SQL, originally called Sequel, as part of the [System R project](https://datacadamia.com/db/systemr) in the early 1970's. The sequel language has evolved since then, and its name has changes to SQL (Structured Query Language). Many products now support the SQL language. SQL has established itself as the standard relational database language. 

In 1986, the American National Standards Institute (ANSI) and the International Organization for Standardization (ISO) published an SQL standard, called SQL-86. ANSI published an extended standard for SQL, SQL-89 in 1989. Next versions are SQL-92, SQL:1999, SQL:2003, SQL:2006, SQL:2008, SQL:2008 R2 and latest being SQL Server 2022. Find more information [here](https://learn.microsoft.com/en-us/troubleshoot/sql/releases/download-and-install-latest-updates). 

#### SQL partitions : 

- [[Data Definition Language]] : 
	The SQL DDL provides commands for defining relation schemas, deleting relations and modifying relational schemas.
- [[Data Manipulation Language]] :
	The SQL DML provides set of commands to fetch data from the database and provides ability to insert tuples into, delete tuples from and modify tuples in the database.
- Integrity : 
	SQL DDL commands includes commands for specifying integrity constraints that the data being stored in database must follow. Updates that violates this data integrity constraints are disallowed. 
- [[Views]] : 
	SQL DDL includes commands for defining views. 
- Transaction Control : 
	SQL contains commands to specify beginning and ending of a transaction.
- Embedded SQL and Dynamic SQL : 
	Embedded and Dynamic SQL define how SQL statements can be embedded withing general purpose programming languages.
-  Authorization : 
	The SQL DDL includes commands for specifying access rights to relations and views. 