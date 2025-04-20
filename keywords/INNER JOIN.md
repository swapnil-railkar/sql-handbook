tags : #join 

#### Introduction : 

INNER JOIN is used to join two tables, returning only those records which satisfies given join condition. While INNER JOIN is commonly used in foreign key relationships, it can also be applied to other types of column relationships.

#### Syntax :

```
SELECT attribute1, attribute2, ...
FROM table_name1 INNER JOIN table_name2
ON condition;
```

For example consider;

```
SELECT instructor.name, course.title
FROM instructor INNER JOIN course
ON instructor.department_name = course.department_name;
```

The resulting relation will only contain tuples which have matching *department_name* entry in both #instructor  and #course relation. That is, result will not contain *chemistry* tuple from #course 