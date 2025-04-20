tags : #join 

#### Introduction : 

NATURAL JOIN is a type of join that automatically joins tables based on all columns with the same name and compatible data types in both tables. Unlike explicit joins like INNER JOIN or LEFT JOIN, where you specify the condition explicitly, the NATURAL JOIN automatically matches columns with the same name in both tables. 

#### How it works ? 
- It automatically identifies the columns that have the same names in both tables.
- It performs an INNER JOIN on those columns, but it eliminates duplicate columns in the result (columns with the same name will appear only once).
- Column names must be the same in both tables for a NATURAL JOIN to work.
- The NATURAL JOIN is like an INNER JOIN, meaning only rows with matching values in the common columns will be included in the result.
- If you don't want to join on all columns with the same name, you should use an explicit join.

#### Syntax : 

```
SELECT attribute_1, attribute_2, ...
FROM table_1 
NATURAL JOIN table_2;
```

For example, NATURAL JOIN for #instructor and #course will result in : 

| id  | name | department_name | salary | course_id | title | credits |
| --- | ---- | --------------- | ------ | --------- | ----- | ------- |
|     |      |                 |        |           |       |         |
