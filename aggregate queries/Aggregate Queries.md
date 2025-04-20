tags : #dml #aggregate 

#### Introduction : 

Aggregate queries are used to aggregate the data obtained from [[Data Manipulation Language]]. Aggregate functions are set of functions that take a collection of  values as input and produces a single value as output.

#### SQL Built-in aggregate functions : 

1. Average : [[AVG]]
2. Maximum : [[MAX]]
3. Minimum : [[MIN]]
4. Total : [[SUM]]
5. Count : [[COUNT]]

#### Aggregation with grouping : 

In the circumstances where we have to apply aggregation not only to single set of tuple but group of set of tuples, we use [[GROUP BY]] clause. The attribute or attributes given in [[GROUP BY]] clause are used to form groups. Tuples with same value on attribute specified in [[GROUP BY]] clause are placed in same group.


---

 **Why we can not use aggregate functions in WHERE condition ?** 
	WHERE operates on individual rows before aggregating, hence we can use WHERE condition to control the output of aggregation functions. HAVING clause works on result of aggregation. Therefore we cannot use aggregate functions in WHERE clause but they can be used in HAVING clause.

Also read : [[HAVING]] clause.
