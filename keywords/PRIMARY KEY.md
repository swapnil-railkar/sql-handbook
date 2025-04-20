tags : #ddl #keyword 

#### Introduction : 

Primary key is attribute in any relation which can be used to uniquely identify a tuple. Attributes used for primary key should be non null and it should have unique values for given relation. If more than one attributes are getting used for primary key, then all combinations of the candidate attributes should be unique as well. 

#### Defining primary key for relation : 

One way of defining any attribute as primary key is as follows : 

```
CREATE TABLE table_name (
	attribute_name_1 data_type PRIMARY KEY,
	attribute_name_2 data_type constraint (optional)
	.
	.
	.
	attribute_name_n data_type constraint (optional)
);
```

for example, to define *id* as primary key for relation #instructor , we can do following : 

```
CREATE TABLE instructor (
	id INT PRIMARY KEY,
	name VARCHAR(255) NOT NULL,
	department_name VARCHAR(255),
	salary INT
);
```

Another way of defining any attribute as primary key is : 

```
CREATE TABLE table_name (
	attribute_name_1 data_type PRIMARY KEY,
	attribute_name_2 data_type constraint (optional)
	.
	.
	.
	attribute_name_n data_type constraint (optional),
	PRIMARY KEY(attribute_name_1)
);
```

above example defines *attribute_name_1* as primary key of relation. To define *id* as primary key in this way we can do following : 

```
CREATE TABLE instructor (
	id INT,
	name VARCHAR(255) NOT NULL,
	department_name VARCHAR(255),
	salary INT,
	PRIMARY KEY(id)
);
```

Note that, any attribute defined as primary key is *not null* and *unique* by default. This constraints are imposed on the attribute DBMS itself. Hence explicitely defining this constraints on attribute selected as primary key is redundant. 

