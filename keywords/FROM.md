tags : #dml 

#### Introduction : 

FROM keyword is used to define one or more relations to fetch data from. If there are more than one relation defined however, we should use [[Join Queries]]. 

#### Syntax : 

```
SELECT attribute(s) 
FROM table_name;
```

Example : 

```
SELECT *
FROM instructor;
```

Above query will fetch all data for all attributes from relation #instructor 

Output : 

| id  | name | department_name  | salary |
| --- | ---- | ---------------- | ------ |
| 1   | John | computer science | 2000   |
| 2   | Doe  | finance          | 2500   |
| 3   | Marc | history          | 1000   |

Example : 

```
SELECT *
FROM department;
```

Above query will fetch all data for all attributes from relation #department 

Output : 

| dept_name        | building | budget |
| ---------------- | -------- | ------ |
| computer science | B101     | 20000  |
| finance          | B102     | 10000  |
| history          | B103     | 15000  |

