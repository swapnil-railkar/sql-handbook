tags : #join 

#### Introduction : 

Result of FULL JOIN is combination of the result of LEFT JOIN and RIGHT JOIN. It returns all rows from both tables, matching rows where possible. If there is no match, the will still include all rows from both tables, with NULL values in the columns where there is no match.
FULL JOIN gives you a complete result set with no data loss, showing all rows from both tables even if they didn't match.

#### Syntax : 

```
SELECT attribute1, attribute2, ...
FROM table1
FULL JOIN table 2
ON condition;
```

