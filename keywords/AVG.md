tags : #aggregate 

#### Introduction : 

AVG keyword is used to find average value of attribute defined in function. Result of AVG can be controlled using a [[WHERE]] condition.  AVG keyword can only be applied to attributes with numeric value.

#### Syntax : 

```
SELECT AVG(attribute_name)
FROM table_name
WHERE condition;
```

Example : 
Consider query "Display average salary of instructor in computer science department".

```
SELECT AVG(salary)
FROM instructor
WHERE department_name = 'computer science';
```

#### Using average value in conditions : 

SQL does not allow usage of AVG with [[WHERE]] condition but it can be used in [[HAVING]] clause to use as condition.

Example : 
Consider query "Display department names having instructors with average salary greater than  3500".

```
SELECT department_name, AVG(salary) as avg_salary
FROM instructor
GROUP BY department_name
HAVING AVG(salary) > 3500;
```

To use average value with [[WHERE]], we have to use [[Sub Queries]]. Consider query " Display name of instructor who earns more than average salary".

```
SELECT name
FROM instructor
WHERE salary > (
	SELECT AVG(salary)
	FROM instructor
);
```
