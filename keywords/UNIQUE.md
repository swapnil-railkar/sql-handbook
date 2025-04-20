tags : #ddl #keyword 

#### Introduction : 
UNIQUE keyword is used to add constraint on any attribute so that all tuples will have unique value for that attribute. Attributes with *unique* constraint can have null values. This is because according to database design principles, *null* is not a value and thus is not compared for uniqueness.

#### Syntax : 

While defining a relation 

```
attribute_name data_type UNIQUE other_constraints
```

Altering existing relation to impose unique constraint 

```
ALTER TABLE table_name
ADD CONSTRAINT constraint_name UNIQUE(attribute_name);
```
