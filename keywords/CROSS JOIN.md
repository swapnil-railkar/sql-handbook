tags : #join 

#### Introduction : 

CROSS JOIN is used to find cartesian product of two or more relations. CROSS JOIN join each tuple of left relation to every tuple of right relation, giving all possible combinations of tuples. Suppose two relations have *m* and *n* number of tuples respectively, then the resulting relation of CROSS JOIN will have (m\*n) tuples.
A CROSS JOIN will return large number of rows which is computationally expensive if tables are large. CROSS JOIN does not require any condition to join.

#### Syntax : 

```
SELECT attribute1, attribute2, ...
FROM table1 
CROSS JOIN table2;
```

