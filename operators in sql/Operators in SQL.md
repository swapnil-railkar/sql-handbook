tags :  #operators #dml 

#### Introduction : 

SQL provides set of operators to perform operation on data within the query. They are classified into following categories 
1. Arithmetic operators
2. Comparison operators
3. Logical operators
4. Bitwise operators
5. String operators
6. Special operators


#### 1. Arithmetic operators :

| Operator | Description             | Example        |
| -------- | ----------------------- | -------------- |
| +        | Addition operator       | SELECT 10 + 15 |
| -        | Subtraction operator    | SELECT 15 - 10 |
| *        | Multiplication operator | SELECT 10 * 15 |
| /        | Division operator       | SELECT 15 / 10 |
| %        | Modulus operator        | SELECT 15 % 10 |

#### 2. Comparison operators : 

| Operator | Description                                                                                                                           | Example                                        |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| =        | Equals operator, result is true when left hand side value is equal to right hand side value.                                          | SELECT *  FROM instructor WHERE salary = 5000; |
| != or <> | Not equals operator, result is true when left hand side value is not equal to right hand side value.                                  | SELECT * FROM course WHERE course_id <> 'cs';  |
| >        | Greater than operator, result is true when left hand side value is greater than right hand side value.                                | SELECT * FROM instructor WHERE salary > 5000;  |
| <        | Less than operator, result is true when left hand side value is less than right hand side value.                                      | SELECT * FROM instructor WHERE salary < 5000;  |
| >=       | Greater than or equal to operator, result is true when left hand side value is either greater than or equal to right hand side value. | SELECT * FROM instructor WHERE salary >= 5000; |
| <=       | Less than or equal to operator, result is true when left hand side value is either less than or equal to right hand side value.       | SELECT * FROM instructor WHERE salary <= 5000; |

#### 3. Logical operators : 

| Operator | Description                                                                                                                          | Example                                                                     |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| AND      | Logical AND operator, returns true when both left hand side and right hand side conditions are true.                                 | SELECT * FROM instructor WHERE salary > 1000 AND department_name = history; |
| OR       | Logical OR operator, returns true when either left hand side condition or right hand side condition is true.                         | SELECT * FROM instructor WHERE salary > 1000 OR department_name = history;  |
| NOT      | Logical NOT operator. It negates the result of condition, that is, it returns true when result of condition is false and vice versa. | SELECT * FROM course WHERE NOT course_id = 'cs';                            |

#### 4. Bitwise operators : 

| Operator | Description          | Example         |
| -------- | -------------------- | --------------- |
| &        | Bitwise AND operator | SELECT 10 & 15; |
| ^        | Bitwise XOR operator | SELECT 10 ^ 15; |
| ~        | Bitwise NOT operator | SELECT ~15;     |

#### 5. String operators : 

| Operator           | Description                                                 | Example                                                           |
| ------------------ | ----------------------------------------------------------- | ----------------------------------------------------------------- |
| LIKE               | This operator is used for case sensitive pattern matching   | SELECT * FROM instructor WHERE  department_name LIKE 'computer%'; |
| ILIKE (postgreSql) | This operator is used for case insensitive pattern matching |                                                                   |
read more : [[String operations]]
#### 6. Special operators : 

| Operator | Description                                                                                                                                                          | Example                                                       |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| BETWEEN  | This operator return true when value is in between specified inclusive range. This operator is usually used in combination with AND operator                         | SELECT *  FROM instructor WHERE salary BETWEEN 1000 AND 5000; |
| IN       | This operator return true when value is included in list of values.                                                                                                  | SELECT *  FROM course WHERE course_id IN ('cs', 'fin');       |
| EXISTS   | This operator returns boolean value as result if some value exists for given query. This operator is usually used to check whether sub query is returning any record |                                                               |
| IS NULL  | This operator return true when value for specified attribute is null for given query.                                                                                | SELECT * FROM instructor WHERE  department_name IS NULL       |
| NOT NULL | This operator return true when value for specified attribute is not null for given query.                                                                            | SELECT * FROM instructor WHERE  department_name NOT NULL      |

