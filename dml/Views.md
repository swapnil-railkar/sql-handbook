tags : #dml 

#### Introduction : 

It is not desirable for all users to see the entire logical model. Security considerations may require that certain data be hidden from users. SQL allows virtual relation to be defined by a query , and the result conceptually contains the result of the query. The relation is not precomputed or stored, but instead is computed by executing the query whenever the virtual relation is used.

#### Syntax : 

We define a view in SQL by using the *create view* command. To define a view, we must give the view a name and must state the query that computes the view. The from of the *create view* command is : 

```
CREATE VIEW view_name AS (query expression);
```

where *query expression* is any legal query expression.

For example, a clerk may need to access data of all instructors and we wish he should not have access to fetch salary of instructor. To achieve this we can define a view named *faculty* and making it available for clerk instead of instructor relation. We can define view *faculty* as :

```
CREATE VIEW faculty AS 
SELECT id, name, department_name
FROM instructor;
```

#### Using views in SQL queries : 

Once we have defined a view, we can use the view name to refer to the virtual relation that the view generates. View names can appear in a query any place where a relation name may appear.

```
SELECT *
FROM faculty;
```

The attribute names of a view can be specified explicitly as follows : 

```
CREATE VIEW total_salary(department_name, total_salary) AS
SELECT department_name, SUM(salary)
FROM instructor
GROUP BY department_name;
```

It gives for each department the sum of the salaries of all the instructors at that department. Since *SUM(salary)* does not have a name, the attribute name is specified explicitly in view definition.

When we define a view, the database system stores the definition of view itself, rather than the result of evaluation of the query expression that defines the view. Wherever a view relation appears in a query it is replaced by stored query expression. Thus, whenever we evaluate the query, the view relation is recomputed.

#### Materialized views : 

Certain database systems allow the view relations to be stored, but they also make sure that when the actual relation gets updated, the view is kept up to date. Such views are called **materialized views**. 

The process of keeping the materialized view up to date is called **view maintenance**. View maintenance can be done immediately when any of the relation on which view is defined is updated. Some database systems, however, perform view maintenance lazily, when the view is accessed. Some system update materialized view periodically. In this case the contents of materialized view may be stale, and should not be used if the application needs up to date data. 

#### Update of a view : 

Although views are useful tool for queries, they present serious problems if we express updates, insertions or deletions with them. The difficulty is that a modification to database expressed in terms of view must be translated to a modification to the actual relations in the logical model in the database. 

SQL view is said to be updatable if the following conditions are all satisfied by the query defining the view : 
- The FROM clause has only one database relation.
- The SELECT clause contains only attribute names of the relation, and does not have any expression, aggregates or distinct specifications.
- Any attribute not listed in the SELECT clause can be set to *null*, that is, it does not have a *not null* constraint and is not part of primary key.
- The query does not have a GROUP BY or HAVING clause.
