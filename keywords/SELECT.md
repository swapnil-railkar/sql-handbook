tags : #dml 

#### Introduction : 

SELECT keyword is used to fetch data from one or more relations. SELECT keyword allows user to define attributes for which data should be fetched. '\*'  is used to define 'all attributes', if user want to see data for all attributes in given query. SELECT is used in conjunction with [[FROM]] to define relation from which data should be fetched.

#### Syntax : 

```
SELECT attribute_name1, attribute_name2, ...
FROM table_name;
```

Example : 

```
SELECT name, salary
FROM instructor;
```

above query will show all data for attributes *name* and *salary* from relation #instructor 

Output ;

| name | salary |
| ---- | ------ |
| John | 2000   |
| Doe  | 2500   |
| Marc | 1000   |

Example : 

```
SELECT * 
FROM instructor;
```

above query will show all data for all attributes from relation #instructor 

Output : 

| id  | name | department_name  | salary |
| --- | ---- | ---------------- | ------ |
| 1   | John | computer science | 2000   |
| 2   | Doe  | finance          | 2500   |
| 3   | Marc | history          | 1000   |
