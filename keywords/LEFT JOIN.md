tags : #join 

#### Introduction : 

LEFT JOIN is used to join two tables, returning all records from left table and only matching records from right table based on given join condition. If there is no match, columns from the right table will be filled with *null* values. While LEFT JOIN is commonly used in foreign key relationships, it can also be applied to other types of column relationships. 

#### Syntax : 

```
SELECT attribute1, attribute2, ...
FROM table_name1 LEFT JOIN table_name2
ON condition;
```

For example consider; 

```
SELECT instructor.name, course.title
FROM instructor LEFT JOIN course
ON instructor.department_name = course.department_name;
```

Above query will join #instructor and #course for matching attribute on *department_name*. The resultant relation will look like this

| id  | name | department_name | salary | course_id | title | department_name | credits |
| --- | ---- | --------------- | ------ | --------- | ----- | --------------- | ------- |
|     |      |                 |        |           |       |                 |         |

Above relation will contain all tuples from #instructor relation but tuple for *chemistry* department name will not be included in the resulting relation as #department do not have any tuple for *chemistry*.




