tags : #ddl #keyword 

#### Introduction : 
ALTER TABLE command is used to modify existing relation. ALTER TABLE command can be used to add attribute / constraint in the relation, edit existing attribute / constraint in the relation or remove attribute / constraint in the relation. 

Consider relation #instructor for following examples.
#### Syntax : 

- Altering attributes of relation

1. Add new attribute in relation. 

```
ALTER TABLE table_name
ADD attribute_name data_type constraint (optional);
```

Example : 

```
ALTER TABLE instructor 
ADD contact_number INT NOT NULL;
```

2. Edit attribute in relation.

```
ALTER TABLE table_name
ALTER COLUMN attribute_name TYPE new_data_type;
```

Example : 

```
ALTER TABLE instructor 
ALTER COLUMN contact_number TYPE BIGINT;
```

3. Rename attribute in relation.

```
ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;
```

Example : 

```
ALTER TABLE instructor 
RENAME COLUMN contact_number TO contact_info;
```

4. Remove existing attribute in relation

```
ALTER TABLE table_name
DROP COLUMN attribute_name;
```

Example : 

```
ALTER TABLE instructor 
DROP COLUMN contact_info;
```

5. Rename relation 

```
ALTER TABLE old_table_name
RENAME new_table_name;
```

Example : 

```
ALTER TABLE instructor
RENAME tutor;
```

- Altering constraints on relation

1. Add constraint

```
ALTER TABLE table_name
ADD CONSTRAINT constraint_name constrain_name (attribute_name);
```

Example : 

```
ALTER TABLE instructor 
ADD CONSTRAINT unique_name UNIQUE (name);
```

2. Drop constraint

```
ALTER TABLE table_name
DROP CONSTRAINT constraint_name;
```

Example : 

```
ALTER TABLE instructor 
DROP CONSTRAINT unique_name;
```

