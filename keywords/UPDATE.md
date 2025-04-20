tags : #dml 

#### Introduction : 

UPDATE keyword is used to update existing entries in given relation. It cannot be used to insert new tuple but can only be used to update the values in existing tuples. The updating of data can be constrained by using a [[WHERE]] clause. Only the values which satisfies the condition in where clause will get updated. If we do not constraint the UPDATE keyword, entire relation will get updated.

#### Syntax : 

```
UPDATE table_name
SET attribute_name1 = value1, attribute_name2 = value2, ...
WHERE condition;
```

Example : 

```
UPDATE department
SET budget = 20000
WHERE department_name = 'history';
```

Above query will update the value of *budget* attribute from *department* relation where *department_name* is history.

Output : 

| department_name | building | budget |
| --------------- | -------- | ------ |
| history         | B103     | 20000  |