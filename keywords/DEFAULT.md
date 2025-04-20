tags : #ddl #keyword 

#### Introduction : 

DEFAULT keyword is used to predefine a value for any attribute. Attribute will be stored with that value if no value is explicitly defined in query. DEFAULT keyword is used, as the word suggests, give default value to attribute  in case no value is defined. Attribute with DEFAULT constraint will store null values only if it is defined explicitly in insert query.

#### Syntax : 

While defining a relation

```
attribute_name data_type DEFAULT default_value
```

Altering existing relation to define default value 

```
ALTER TABLE table_name
ALTER COLUMN attribute_name SET DEFAULT default_value;
```

