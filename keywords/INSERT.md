tags : #dml

#### Introduction :

INSERT keyword is used to (u guessed it right!!) insert data into any given relation. While using insert query, all constraints on every attribute should be satisfied else it will return with error and aborts insert operation. We can insert one or more tuples using single INSERT query.

- Inserting single tuple : 
#### Syntax : 

```
INSERT INTO table_name(attribute1, attribute2, ..., attributeN)
VALUES(value1, value2, ..., valueN);
```

Example : 

```
INSERT INTO instructor(id, name, department_name, salary)
VALUES(4, 'Walter', 'chemistry', 3000);
```

Output : 

| id  | name   | department_name | salary |
| --- | ------ | --------------- | ------ |
| 4   | Walter | chemistry       | 3000   |
- Inserting multiple tuples : 

```
INSERT INTO table_name(attribute1, attribute2, ..., attributeN)
VALUES
(value1, value2, ..., valueN),
(value1, value2, ..., valueN),
(value1, value2, ..., valueN)
.
.
.
;
```

Example : 

```
INSERT INTO department(department_name, building, budget)
VALUES
('geography', 'B103', 20000),
('music', 'B104', 17000),
('arts', 'B104', 17000);
```

Output : 

| department_name | building | budget |
| --------------- | -------- | ------ |
| geography       | B103     | 20000  |
| music           | B104     | 17000  |
| arts            | B104     | 17000  |