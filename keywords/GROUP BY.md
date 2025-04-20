tags : #aggregate 

#### Introduction : 

GROUP BY clause is used to apply aggregate function to group of set of tuples. The attribute or attributes given in GROUP BY clause are used to form groups. Tuples having same value on all attributes in the GROUP BY clause  are placed in same group. **Any attribute that is not present in GROUP BY clause must only appear inside aggregate function if it appears in SELECT clause. Otherwise query is treated as erroneous.**

#### Syntax : 

```
SELECT attrbute_1,...
FROM table_name
GROUP BY attribute_1,...;
```

Consider query, "Find average salary of each department."

```
SELECT department_name, AVG(salary) as avg_salary
FROM instructor
GROUP BY department_name;
```

Consider following example ; 

```
/* erroneous query */
SELECT department_name, id, AVG(salary) as avg_salary
FROM instructor
GROUP BY department_name;
```

Above query will be treated as erroneous because attribute *id* appears in SELECT clause but neither occur inside GROUP BY nor it is a part of an aggregate function.







