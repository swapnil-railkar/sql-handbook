tags : #aggregate 

#### Introduction :

MIN keyword is used to find out minimum value of attribute defined in function. Result of MIN keyword can be controlled using [[WHERE]] clause. MIN keyword can only be applied to attributes with numeric value.

#### Syntax :

```
SELECT MIN(attribute_name)
FROM table_name
WHERE condition;
```

Consider query, "Display minimum salary earned by instructor in finance department".

```
SELECT MIN(salary)
FROM instructor
WHERE department_name = "finance";
```

#### Using maximum value in condition :

SQL does not allow usage of AVG with [[WHERE]] condition but it can be used in [[HAVING]] clause to use as condition. Consider query "Display department names having instructor with minimum salary".

```
SELECT department_name, MIN(salary) as min_salary
FROM instructor
GROUP BY department_name
HAVING salary = MIN(salary);
```

To use average value with [[WHERE]], we have to use [[Sub Queries]]. Consider query "Display name of instructor who earns minimum salary".

```
SELECT name
FROM instructor
WHERE salary = (
	SELECT MIN(salary)
	FROM instructor
);
```