tags : #ddl #keyword 

#### Introduction : 

When we introduce an attribute in a relation (say r1) which is already a primary key for any other relation (say r2), then we call the attribute as foreign key referring r2 from r1. Foreign keys are generally used to showcase relation in different tables in database. Foreign keys becomes handy when joining relations. It is common practice to keep foreign keys as non null but it is not compulsory constraint.

#### Defining foreign key in relations : 

Consider following relation : 

| dept_name        | building | budget |
| ---------------- | -------- | ------ |
| computer science | B101     | 20000  |
| finance          | B102     | 10000  |
| history          | B103     | 15000  |
*table* : #department

Suppose this relation uses *dept_name* attribute as primary key. Now we can say that *dept_name* is foreign key in relation #course referencing to relation #department 

#### Example : 

We can use following command to create relation #department 

```
CREATE TABLE department (
	dept_name varchar(255),
	building varchar(100),
	budget INT,
	primary key(dept_name)
);
```

Now, defining *dept_name* as foreign key in relation #course .

**Scenario 1** : 
If one does not have #course relation defined in database 

```
CREATE TABLE course (
	course_id varchar(100),
	title varchar(255),
	department_name varchar(100) NOT NULL,
	credits INT,
	primary key(course_id),
	foreign key(department_name) references department(department_name)
);
```



**Scenario 2** :
If #course relation is already defined in database, then we have to alter the relation to add *department_name* attribute and then add constraint to define it as foreign key.

```
-- add column department_name in course relation.
ALTER TABLE course
ADD department_name varchar(100) NOT NULL;

-- add constraint to define department_name as foreign key.
ALTER TABLE course
ADD CONSTRAINT department_fk
FOREIGN KEY(department_name)
REFERENCES department(department_name);
```

In both above examples we apply foreign key constraint on attribute *department_name* and defines that it refers to *department_name* of #department relation for which that attribute is primary key. Note that *department_name* also have constraint NOT NULL, which is not compulsory but it is a good practice to do so.
