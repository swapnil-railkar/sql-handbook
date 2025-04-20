tags : #join 

#### Introduction : 

SELF JOIN is used to join the table  with itself. This is useful when we want to compare rows within the same table. We essentially create tow aliases for the same table and join them on a condition that matches rows in different ways.

#### Syntax : 

```
SELECT a.attribute_1, b.attribute_2
FROM table_name a 
JOIN table_name b
ON condition;
```

For example, joining #course table will result in relation like : 

| course_id | title | department_name | credits | course_id | title | department_name | credits |
| --------- | ----- | --------------- | ------- | --------- | ----- | --------------- | ------- |
|           |       |                 |         |           |       |                 |         |

Self joins are useful in hierarchical data like employee-manager relationships, parent-child relationships etc. 

