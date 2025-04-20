tags : #aggregate 

#### Introduction :

COUNT is used to count the number of tuples. If any condition is provided, then it will count number of tuples that satisfies given condition. 

#### Syntax : 

```
SELECT COUNT(attribute_name)
FROM table_name
WHERE condition;
```

- COUNT with SELECT
	Consider query, "Count all courses"

```
SELECT COUNT(course_id)
FROM course;
```

- COUNT with condition 
	Consider query, "Count all instructors with salary more than 2000"


```
SELECT COUNT(id)
FROM instructor
WHERE salary > 2000;
```

- Grouped COUNT 
	Consider query, "count instructors in each department."

```
SELECT department_name, COUNT(id)
FROM instructor
GROUP BY department_name;
```


- COUNT as condition 
	As COUNT is aggregate function hence it cannot be used in WHERE clause. If we want to use COUNT as condition we can use it with HAVING clause.
	Consider query "get department names with more than three instructors."

```
SELECT department, COUNT(id) as emp_count
FROM instructor
GROUP BY department
HAVING COUNT(id) > 3;
```



---

COUNT(\*) will count all rows, including the NULL valued tuples while COUNT(attribute_name) will only count tuples having non null values for given attribute.


