tags : #ddl 

#### Introduction : 

Data Definition Language (DDL) refers to set of commands used to define the structure of data to be stored in given database. This set of command are used to define or alter the structure of table. The set of relations in a database must be specified  to the system by means of a data definition language. 


#### DDL functionalities : 

The SQL DDL not only allows user to define relations but also
- Schema definition for each relation.
- Type of values associated with each attribute.
- The integrity constraints.
- The set of indices to be maintained for each relation.
- The security and authorization information for each relation.
- The physical storage structure of each relation on disk.

#### Data types supported by SQL : 

**Numeric data types** : 
	Numeric data types are used to store numbers and include
- BIT : Store either 0 or 1.
- TINYINT : Store value from 0 to 255.
- SMALLINT :  Stores values from -32,768 to 32,767.
- INT : Stores values from -2,147,483,648 to 2,147,483,647.
- BIGINT : Stores values from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
- DECIMAL and NUMERIC : Both can store values from -10^38 + 1 to 10^38 - 1.
- FLOAT : Stores floating point numbers from -1.79E+308 to 1.79E+308.
- REAL : Stores floating point numbers from -3.40E+38 to 3.40E+38.

**String data types** : 
	String data types used to store string or character sequence and include 
- VARCHAR(n) : Stores character string varying in length. String can have at most *n* characters.

**Binary data types** : 
	Used to store binary data 
- BINARY(n) : Stores fixed length binary data and unused space is padded with zeroes.
- VARBINARY(n) : Stores binary data of varying length. Unused spaced does not get padded. Can store at max *n* bytes.
- BLOB : Binary Large Object (BLOB) is used to store large binary objects like images, audios and videos. Available in different size based on database system.


#### Common DDL commands : 

- Commands that works on structure of relation : 
	1. [[CREATE]]
	2. [[ALTER]]
	3. [[DROP]]
	4. [[TRUNCATE]]
	5. [[COMMENT]]

- Commands that allows to specify constraints on data for integrity : 
	1. [[PRIMARY KEY]]
	2. [[FOREIGN KEY]]
	3. [[UNIQUE]]
	4. [[NOT NULL]]
	5. [[CHECK]]
	6. [[DEFAULT]]
