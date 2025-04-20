tags : #join 

#### Introduction : 

RIGHT JOIN is used to join two tables, returning all records from right table and only matching records from left table based on given join condition. If there is no match, columns from the right table will be filled with *null* values. While RIGHT JOIN is commonly used in foreign key relationships, it can also be applied to other types of column relationships.

#### Syntax : 

```
SELECT attribute1, attribute2, ...
FROM table_name1 RIGHT JOIN table_name2
ON condition;
```

For example consider; 

```
SELECT instructor.name, course.title
FROM instructor RIGHT JOIN course
ON instructor.department_name = course.department_name;
```

Above query will join #instructorand and #coursefor matching attribute on _department_name_. The resultant relation will look like this

|id|name|department_name|salary|course_id|title|department_name|credits|
|---|---|---|---|---|---|---|---|
|||||||||

Above relation will contain all tuples from #department relation but tuple for department name *chemistry* will have null values for #instructor attributes as #department do not have any tuple for *chemistry*.