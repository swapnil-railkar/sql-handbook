tags : #dml

#### Introduction : 

WHERE keyword is used to define conditions or filters, for example, data being fetched from relation defined in [[FROM]]. Most of [[Operators in SQL]] are used in WHERE clause. WHERE keyword allows user to define a filter on data by using conditions, for example, only the tuples in relation which passes this condition will appear in result of [[SELECT]]. WHERE keyword is also used with [[UPDATE]] and [[DELETE]] to filter the tuples on which defined operation should be performed. 

#### Syntax : 

```
SELECT attribute_name(s)
FROM table_name
WHERE condition;
```

Example : 

```
SELECT name 
FROM instructor
WHERE salary > 1500;
```

Above query will filter the tuple for which the value of *salary* attribute is greater than 1500.

Where clause can support more than one conditions using logical operators (read more about them in [[Operators in SQL]]). For example, 

```
SELECT name
FROM instructor
WHERE salary < 2000 AND department_name = 'finance';
```

Above query will filter the tuples from relation #instructor for which *salary* is less than 2000 and have *department_name* as finance.

