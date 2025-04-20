tags :  #introductionToSQL 

####  Introduction : 

One of the main characteristic of data is that it grows, so one can always store as much of data as desired, but this vast storage of data will serve no great purpose if it is not collected and organized properly.  RDBMS (Relational Database Management System) is, as the name suggests, database management systems that supports relational model. Relational databases provide huge benefits for collecting and organizing the data and hence maximizes the potential of stored data. As relational databases stores data in table like structure where all related data points are stored in a row (tuple), it reduces the complexity and helps in storing, manipulating and retrieving the data effectively.

#### Advantages of RDBMS : 

1. Data accuracy : 
	Databases often are prone to errors like duplication. Duplication occurs when identical data is stored multiple time unintentionally (Not to be confused with *Redundancy* where user intentionally store multiple copies of same data to ensure availability of data. This duplication is controlled duplication and is often supervised by designers). Data duplication results in wastage of space and slow query speed and most important,  inaccurate results.
	
	RDBMS helps to ensure accuracy of data stored by : 
	- Using integrity constraints (primary key, foreign key etc.)
	- Using [[ACID Transactions]] to maintain consistency.
	- Using [[Normalizations]] to prevent duplication.

2. Data integrity : 
	Data integrity is a concept and process that ensures accuracy, completeness, validity and reliability of organization's data. Relational databases often have data typing and validity checks that ensures the is entered correctly based on predetermined criteria. 
	
	User can impose data integrity checks on data being stored in database using [[Data Definition Language]]. It also warns when data is missing, making sure the information is complete. As in relational database, tables rely on one another to function, it guarantees accuracy and consistency by removing imperfection and isolation.
	
3. High security :
	The term 'security' in reference to databases refers to constraints that allow one to access and/or modify only the data they have permission to access. "Database security refers to tools, controls and measures designed to establish and preserve database confidentiality, integrity and availability.", according to [source](https://www.ibm.com/think/topics/database-security).
	
	Read more : [[Relational Databases and Security]].
	
4. Easy to access :
	Relational databases uses [[SQL(Structured Query Language)]] to access data stored within. SQL allows user to use relational algebra to combine two or more tables easily and hence data access and manipulation simpler. As RDBMS imposes [[ACID Transactions]], it allows multiple users to access data simultaneously while DBMS takes care of data accuracy and integrity.
	 
	Unlike other models, there is no hierarchical pattern or pathway for obtaining data. Anyone with access to database can easily navigate it, querying any table and combining information from multiple tables to fetch and analyze exact details they need.
	
5. Future modification :
	Relational databases can be modified easily as per the requirements. The attribute which are required to be stored changes frequently as per the business needs, [[Data Definition Language]] makes it easier to add or remove an attribute in relation without modifying existing data in relational database. User can also add or remove existing constraints on any attribute without harming existing data. 
	
6. Flexibility : 
	Once you have implemented a relational database, you can still edit and refine it. This can be done event the tool is working, enabling you to change things as you go without interrupting business processes. So if your business expands or evolves, your database cab too, and you are not bound by rigid structures that were decided by someone long time ago. In relational database you can always add more relations or attributes to suit business need and there is no limitations on number of tuples to be saved. Removing attributes, tuples and relations can be also done easily.
	
7. Simplicity : 
	Even if relational databases are robust and flexible, they are not complex in nature. While other types of databases may require years of training or an ability to write code, relational databases are free hierarchical architecture, storing data in table like structure. Simple [[SQL(Structured Query Language)]] queries can retrieve all the data you need while also utilizing relational algebra. As data is stored in table like structure it is easy to visualize and learn.
	 
8. [[Normalizations]] 

#### Disadvantages of RDBMS : 

1. Cost : 
	Setting up and maintaining a database is a expensive affair and hence becomes one of the biggest disadvantage of RDBMS. The specific software needed to create and configure a relational database are costly. Updating all the information to get the program up and running can also be difficult, and especially so if your organization is a large one with a complex database. In which case, integrating database with any programming language becomes a tedious task. In such cases getting help from more experienced programmers becomes necessity.
	 
	You will also need to have an expert RDBMS administrator for managing and controlling the database.
	
2. Lack of speed :
	Compared to other alternatives, RDBMS retrieves data pretty slowly, and therefore, performance is much slower. This is considered as tradeoff for its ease of use and rich functionality.
	
3. Memory requirements : 
	As RDBMS stores data in form of rows and columns, it requires much more physical memory space than its alternatives. This directly affects the business by adding more physical memory cost and is a significant. Relational databases are difficult to scale due to their relational nature. For read-heavy systems, this problem can be solved by using redundancy. But for write-heavy systems, only solution is vertical scaling that is adding more CPU or RAM to database or purchasing larger servers.
	
4. Time consuming setup : 
	To use a relation it's structure and type of data to be stored in relation must be defined
	before we can start storing data in relation, hence it takes more time to setup as each relation must be defined before we can start using it. This becomes a tedious task if requirements are not clear.


---
#### References : 

5. [List of advantages](https://www.easasoftware.com/insights/8-advantages-of-a-relational-database/). 
6. [List of disadvantages](https://webandcrafts.com/blog/advantages-disadvantages-rdbms).