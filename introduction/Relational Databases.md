tags : #introductionToSQL 

#### Introduction : 

Relational database is way of managing data points which are related to one another. Relational databases provide a straightforward way of storing data in form of tables and is preferred by many developers for their personal projects as well as for industry level projects because of its easy implementation and convenience in data retrieval. 

Relational database provides separation of logical data structure (the way in which data is stored, in this case, in form of tables) and physical storage structure (the way in which data is going to be stored in database, generally handled by DBMS providers like [[PostgreSQL]], [[MYSQL]] etc.). For example user can change the name of database without directly affecting the tables stored within. *Logical operations* enables users to specify the data which is needed and *physical storage structure* defines how to access this data then carries out the task. To ensure that data in database is always accurate and accessible user can enforce some integrity rules using [[Data Definition Language]].

#### Example : 

A relational database consists of collection of tables, with unique names. For example consider table #instructor . This table consists of four columns namely id, name, department_name and salary. Suppose this table stores information about instructors working in an university.

| id  | name | department_name  | salary |
| --- | ---- | ---------------- | ------ |
| 1   | John | computer science | 2000   |
| 2   | Doe  | finance          | 2500   |
| 3   | Marc | history          | 1000   |
*table* : #instructor 

Similarly, consider table #course that stores information about courses provided by university.

| course_id | title                            | department_name  | credits |
| --------- | -------------------------------- | ---------------- | ------- |
| cs        | introduction to computer science | computer science | 4       |
| fin       | introduction to finance          | finance          | 3       |
| hist      | history of Egypt                 | history          | 3       |
*table* : #course 

adding another table #prereq to store which courses are pre requisites for any course

| course_id | prereq_id |
| --------- | --------- |
| cs        | hist      |
| fin       | hist      |
*table* : #prereq 

#### Relational database and common terminologies : 

We can observe that in table #instructor and #course  each row can be identified by an unique attribute (for #instructor it is *id* and for #course it is *course_id*), hence we can say that #instructor  table shows relationship between a specified *id* and corresponding values for *name*, *department_name* and *salary*.

In general, a row in table denotes relationship among a set of values. Since a table is collection of such relationships, it is called as **relational database**. Thus in relational model, term ***relation*** is used to refer to the table. Term ***tuple*** is used to refer to a row and term ***attribute*** is used to refer to the column. We use term ***relational instance*** to refer to specific instance of a relation and ***relational schema*** to refer to logical design of database.

For each attribute in relation, all possible values for that attribute becomes domain of that attribute. For example, in relation #instructor , the domain of attribute *salary* are all possible values of salary. We require for all attributes of given relationship, the domain should be atomic, that is, values in domain are considered as indivisible units. For example in #course relation, the value of *title* attribute is said to be atomic as it denotes the title of the course and cannot be condensed further, on the other hand, suppose if the relation #instructor had attribute *address* which stores the address of instructor, we can argue that domain of address attribute is not atomic as address can further be broken down into various sub-attributes like street name, room number etc. The *null* value is special type of value which is unknown or does not exists. 

#### Keys : 

We must have a way to uniquely identify a tuple in given relation. This is obtained by applying constraints to a chosen attribute. The values of such attribute (or attributes) should be in such a way that it uniquely identifies the tuple. In other words, no two tuples in given relation are allowed to have same value for all attributes. 

1. Super key : 
	A super-key is set of one more attributes that, taken collectively allows us to uniquely identify a tuple. If attribute K is super-key then so any superset of K. For example in table #instructor combination of id and name is super-key.

2. Candidate key :
	We are often interested in super-keys for which no proper subset is super-key. Such minimal super-keys are called candidate keys. For example in table  #instructor , attribute *id* is candidate key.

3. Primary key :
	Term primary key is used to denote the candidate key that is chosen by database designer as principal means of identifying tuples within a relationship. For example, as relationship #instructor , attribute *id* is only candidate key, it can be used as primary key.  Primary keys should be chosen such  that their values never (or rarely) changes. Read more [[PRIMARY KEY]].

4. Foreign key :
	A relation say r1, may include among its attributes the primary key of another relation, say r2. This attribute is called foreign key from r1, referencing r2. The relation r1 is called referencing relation and relation r2 is called referenced relation. A referential integrity constraint requires that the value appearing in specified attribute of any tuple in the referencing relation should also appear in specified attributes of at least one tuple in referenced relation. Read more [[FOREIGN KEY]].

#### When to use relational database : 

- Relational databases are ideal in situations where user have to process data with thousands of operations per second. If you are doing millions of transactions per second, relational database will slow you down.
- Relational databases are useful when data structures are stable and rarely changes.
- Data relationships are based on [[Normalizations]]. If you want data de-normalized then relational database are not a good choice.
- Relational databases are of great help if user wants to perform complex querying on data available. As every datapoints which are related are mapped accordingly, it becomes easier to get data.

---
#### References

1. [Introduction](https://www.oracle.com/database/what-is-a-relational-database/)
2. [When to use relational database](https://www.dsstream.com/post/what-is-a-relational-database)


