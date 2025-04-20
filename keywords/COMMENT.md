tags : #ddl #keyword 

#### Introduction :

Comments in SQL are used define statements which will not be executed as SQL statement. Comments are usually used to explain working of statement or to stop statement from getting executed. SQL comments can be differentiated as single line comment or multiline comments.

#### Single line comments : 

Single line comments starts with '--'. Statements starting with '--' will be ignored and will not be executed. 

#### Example :

```
-- defining relation instructor
CREATE TABLE instructor (
	id INT NOT NULL,
	name VARCHAR(255) NOT NULL,
	department_name VARCHAR(255),
	salary INT
);
```

In above example, statement 'defining relation instructor' will be ignored and will not be executed as that line starts with '--'.

#### Example : 

```
-- defining relation instructor
CREATE TABLE instructor (
	id INT NOT NULL, -- id of instructor
	name VARCHAR(255) NOT NULL, -- name of instructor
	department_name VARCHAR(255), -- department of instructor
	salary INT -- instructor's salary
);
```

Above example is also a valid scenario as usage of single line comments as everything after '--' is ignored for that line. 

#### Multiline comments : 

Multiline comments in SQL starts with \/* and ends  with \*/. Any lines between starting and closing commands will be ignored. 

#### Example : 

```
/*
Defining relation 'instructor' 
id : integer (not null)
name : string (not null)
depart name : string (not null)
salary : integer
*/
CREATE TABLE instructor (
	id INT NOT NULL,
	name VARCHAR(255) NOT NULL,
	department_name VARCHAR(255),
	salary INT -- instructor's salary
);
```

In above example, multiline comment is used to explain structure of relation 'instructor'. None of the lines explaining structure will get executed as they are surrounded by \/* and \*/

