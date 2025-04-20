tags : #keyword #ddl 

#### Introduction : 
NOT NULL is constraint which prevents storing null value for an attribute.

#### Syntax : 

while defining a relation 

```
attribute_name data_type NOT NULL
```

Altering existing relation to impose not null constraint 

```
ALTER TABLE table name
ADD CONSTRAINT constraint_name NOT NULL(attribute_name);
```

