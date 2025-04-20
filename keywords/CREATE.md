tags : #ddl #keyword 

#### Introduction : 

CREATE TABLE command is used to define a relation. This command is used to define data types of attributes of relation and to define constraints on this attributes.

#### Syntax : 

```
CREATE TABLE table_name (
	attribute_name_1 data_type constraint (optional)
	attribute_name_2 data_type constraint (optional)
	.
	.
	.
	attribute_name_n data_type constraint (optional)
);
```


#### Example : 

Consider relation #instructor , for this relation we can define create table command as, 

```
CREATE TABLE instructor (
	id INT NOT NULL,
	name VARCHAR(255) NOT NULL,
	department_name VARCHAR(255),
	salary INT
);
```

In the above query, *id* has data type INT and constraint NOT NULL,  *name* is string hence  data type is VARCHAR(255), *department_name* is string hence data type is VARCHAR(255) and *salary* attribute is also of INT data type.
