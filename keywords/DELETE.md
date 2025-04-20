tags : #dml

#### Introduction : 

DELETE is used to remove tuples from relation. Like UPDATE keyword, result of DELETE can also be constrained using [[WHERE]]. Without condition, DELETE query will remove all tuples from given relation. DELETE queries remove tuples from relation without affecting the definition of relation. DELETE queries are preferred for conditionalized removal of tuples. In case of removing all tuples, [[TRUNCATE]] is preferred.

#### Difference between DELETE and TRUNCATE : 

| DELETE                                                | TRUNCATE                                                               |
| ----------------------------------------------------- | ---------------------------------------------------------------------- |
| Allows user to define condition for removal of tuple. | All tuples are removed from given relation. No support for conditions. |
| Does not affect definition of relation.               | Does not affect definition of relation.                                |
| DELETE is slower.                                     | TRUNCATE is faster.                                                    |
| Does not reset identity attribute.                    | Resets identity attribute to minimum value defined.                    |
| DML operation                                         | DDL operation                                                          |
Above mentioned are some key differences between DELETE command and [[TRUNCATE]] command.

#### Syntax : 

```
DELETE FROM table_name
WHERE condition;
```

#### Example : 

```
DELETE FROM department
WHERE budget > 15000;
```

Above query will remove tuple from table #department having *budget* greater than 15000.

Output : 

| department_name  | building | budget |
| ---------------- | -------- | ------ |
| finance          | B102     | 10000  |
| history          | B103     | 15000  |