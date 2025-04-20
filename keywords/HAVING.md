tags : #aggregate 

#### Introduction : 

At times it is useful to state a condition that applies to groups rather than to tuples. To express such a query we use HAVING clause of SQL. **SQL applies predicates in the HAVING clause after groups have been formed, so aggregate functions can be used.**

#### Syntax : 

```
SELECT column1, column2, aggregate_function(column3)
FROM table_name
GROUP BY column1, column2
HAVING condition;
```

Consider query, "Get departments where average salary of instructor is more than 2000."

```
SELECT department_name, AVG(salary) as avg_salary
FROM instructor
GROUP BY department_name
HAVING AVG(salary) > 2000;
```

To illustrate the use of WHERE and HAVING clause in same query, consider "Find names of
instructors in computer science department having average salary more than 2500."

```
SELECT name, department_name, AVG(salary) as avg_salary
FROM instructor
WHERE department_name = 'computer science'
GROUP BY name, department_name
HAVING AVG(salary) > 2500;
```





