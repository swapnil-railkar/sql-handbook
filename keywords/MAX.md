tags : #aggregate 

#### Introduction : 

MAX keyword is used to find out maximum value of attribute defined in function. Result of MAX keyword can be controlled using [[WHERE]] clause. MAX keyword can only be applied to attributes with numeric value.

#### Syntax : 

```
SELECT MAX(attribute_name)
FROM table_name
WHERE condition;
```

Consider query, "Display maximum salary earned by instructor in finance department".

```
SELECT MAX(salary)
FROM instructor
WHERE department_name = "finance";
```


#### Using maximum value in condition : 

SQL does not allow usage of AVG with [[WHERE]] condition but it can be used in [[HAVING]] clause to use as condition. Consider query "Display department names having instructor with maximum salary".

```
SELECT department_name, MAX(salary) as max_salary
FROM instructor
GROUP BY department_name
HAVING salary = MAX(salary);
```

To use average value with [[WHERE]], we have to use [[Sub Queries]]. Consider query " Display name of instructor who earns maximum salary".

```
SELECT name
FROM instructor
WHERE salary = (
	SELECT MAX(salary)
	FROM instructor
);
```

