tags : #aggregate 

#### Introduction : 

SUM keyword is used to find addition of all values of attribute defined in function. Result of SUM keyword can be controlled by using [[WHERE]] conditions. SUM keyword can only be applied to attributes with numeric value.

#### Syntax : 

```
SELECT SUM(attribute_name)
FROM table_name
WHERE condition;
```

Consider query "Display total budget".

```
SELECT SUM(budget)
FROM department;
```

Consider query "Total salary of finance instructors".

```
SELECT SUM(salary)
FROM instructor
WHERE department_name = 'finance';
```

#### Using total value in condition : 

SQL does not allow to use SUM in [[WHERE]] condition, but we can use it in [[HAVING]] condition. Consider query "Display departments having total salary greater than 5000".

```
SELECT department_name, SUM(salary) as total_salary
FROM instructor
GROUP BY department_name
HAVING SUM(salary) > 5000;
```

