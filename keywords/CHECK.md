tags : #ddl #keyword 

#### Introduction : 

CHECK keyword is used add constraint on data being stored for that attribute. CHECK keyword allows user to define a condition. If value to be stored in that attribute passes given condition, then only it will be stored, otherwise the operation will be terminated with error. 

#### Syntax :

While defining a relation

```
attribute_name data_type CHECK(condition)
```

Example : 

Suppose for relation #instructor salary should not be less than 0. We can impose this constraint as 

```
salary INT CHECK(salary > 0)
```

Altering existing relation to add checks 

```
ALTER TABLE table_name
ADD CONSTRAINT constraint_name CHECK(condition);
```

For above example, query can be constructed as 

```
ALTER TABLE instructor
ADD CONSTRAINT positive_salary CHECK(salary > 0);
```

