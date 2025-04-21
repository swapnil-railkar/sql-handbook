tags : #dml 

#### Introduction : 

Sub queries are nested queries or queries within queries where result of inner query is used to calculate the result of outer query.  A sub query is any valid SELECT query that returns a relation which can be used in outer query. Sub queries are defined within brackets ( ).

#### Sub queries in SELECT : 

```
SELECT attribute_name1, attribute_name2, ... ,(subquery) AS alias
FROM table_name
WHERE condition;
```

Consider query, "Give name and salary of instructors along with average salary."

```
SELECT name, salary, (SELECT AVG(salary) FROM instructor) AS avg_salary
FROM instructor;
```

Result of inner query *SELECT AVG(salary) FROM instructor* is calculated and then the result is used by SELECT query with alias *avg_salary*.

#### Sub queries in FROM : 

```
SELECT attribute_name1, attribute_name2, ...
FROM (subquery)
WHERE condition;
```

Consider query, "Give name and salary of instructors earning more than average salary."

```
SELECT intructor.name, instructor.salary
FROM instrcutor, (SELECT AVG(salary) AS avg_salary FROM instructor) as avg_table
WHERE instrcutor.salary > avg_table.avg_salary;
```

Resulting relation for query *SELECT AVG(salary) AS avg_salary FROM instructor* contains attribute *avg_salary* and single tuple with value of average salary of all instructors. The resulting relation is then used in WHERE clause to define condition.

#### Sub queries in WHERE : 

```
SELECT attribute_name1, attribute_name2, ...
FROM table_name
WHERE condition CONDITIONAL OPERATOR (sub query);
```

Consider query, "List all **instructors** who belong to departments that **offer at least one course**."

```
SELECT name, department_name
FROM instructor
WHERE department_name IN (SELECT DISTINCT(department_name) FROM course);
```

The subquery *SELECT DISTINCT(department_name) FROM course* finds all *department_name*'s that exists in the course table. Outer query then filters instructor table to include only those instructors who are in one of those departments.

