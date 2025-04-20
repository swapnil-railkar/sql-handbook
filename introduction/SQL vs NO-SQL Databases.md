tags : #introductionToSQL 

#### Introduction : 

NoSQL (there is conflict in predicted full form. Few resources suggests No-SQL as antonym of SQL, that is Not SQL while other resources suggests Not Only SQL) databases supports storage of unstructured data in contradiction to SQL databases which supports storage of structured data. No-SQL databases stores unstructured data using various data structures. Key-value pair stores, document stores and wide column stores are most commonly used NoSQL database structures.

#### Advantages of No SQL databases over SQL databases : 

1. SQL databases allows user to store structured data in form of rows (tuples) and columns (attributes) in a table (relation). While this is best benefit of relational databases (terms SQL databases and relational databases can be used interchangeably as their core meaning is same that is, storing data in structured format), it also resurfaces as drawback as it cannot store unstructured data. NoSQL gives user ability to effectively store and query unstructured data in various data structures like key-value store, document store, wide column store etc. 
2. While SQL databases requires its structures and attributes to be pre defined thus resulting in more setup time, No SQL databases stores unstructured data as it is hence requires less setup time than SQL databases. 
3. No SQL databases can shard data between multiple data sources allowing distributed databases and makes horizontal scaling possible. Data shards can also be replicated on multiple instances for better data availability.
4. Another notable advantage of No-SQL databases over SQL databases is scaling. SQL databases can only be scaled vertically due to its table-like structure. A defect of horizontal scaling is that we can only add more until we hit the ceiling of current technology. We can only expand our CPU or RAM up to certain limit and we are bound to hit the ceiling where we cannot expand it further. And as the space increases, so increases the price of hardware on which it is stored. Hardware and memory capacity it provides is directly proportional to cost of hardware.  On the other hand, No-SQL databases can be scaled horizontally, that is, we can add more instances of available hardware rather than always upgrading current hardware. This property makes No-SQL database an cheaper alternative compared to SQL database.

#### Disadvantages of No SQL databases : 

1. As No-SQL databases are created with primary goal of storing unstructured data, data stored within this databases cannot be easily analyzed. Data analysis becomes hard due to unstructured nature of data as it is used to query large amount unstructured data gathered from different sources and dumped in the database.
2. Each brand of No-SQL database uses its own unique schema. In some cases (such as MongoDB), there is no schema. In still other designs, it resembles relational databases (Cassandra). The problem here is that each unique system has its own strength and weaknesses, which must be learned before choosing the right No-SQL database for the situation at hand.
3. No-SQL databases does not support [[ACID Transactions]], making it less trustworthy than SQL databases.
4. No-SQL databases are largely used for distributed systems and write heavy systems can be supported by having multiple write shard of same data partition. After writing to a shard in distributed system, there is slight delay before that update is transmitted to other replicas to update as well leading to loss of consistency. Reading from un-updated shard leads to retrieval of stale data. This is also called as *Eventual Consistency*.

---

#### References : 

[Short video that explains pros and cons of both SQL and No-SQL database](https://www.youtube.com/watch?v=_Ss42Vb1SU4)

