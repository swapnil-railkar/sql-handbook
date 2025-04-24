tag : #transactions 

#### Introduction : 

Transaction consist of a sequence of query and / or update statements. The SQL standard specifies that a transaction begins implicitly when an SQL statement is executed. One of the following SQL statements must end the transaction : 
- **Commit work** commits the current transaction; that is, it makes the updates performed by the transaction become permanent in the database. After the transaction is committed, a new transaction is automatically started.
- **Rollback work** causes the current transaction to be rolled back; that is, it undoes all the updates performed by the SQL statements in the transaction. Thus, the database state is restored to what it was before the first statement of transaction was executed.
Transactions in SQL follows [[ACID Transactions]] properties.

#### Transaction rollback and commit : 

Transaction rollback is useful if some error condition is detected during execution of transaction. Commit is similar to saving changes to a document that is being edited, while rollback is similar to quitting edit section without saving changes. Once a transaction is committed, its effects can no longer be undone by rollback. The database system guarantees that even in the event of some failure, such as an error in one of the SQL queries, a power outage or a system crash, a transaction's effects will be rolled back if it has not yet committed. In this case, rollback occurs when system restarts. By either committing the actions of a transaction after all its steps are completed, or rolling back all its actions in case the transaction could not complete all its action successfully, the database provides an abstraction of transaction as being **atomic**. In many SQL implementations, by default, each SQL statement is taken to be as transaction on its own, and gets committed as soon as it is executed. 

#### States of a transaction : 

- **Active** : 
	The initial state. Transaction stays in this state while it is executing.
- **Partially committed** : 
	After final statement has been executed.
- **Failed** :
	After the discovery that normal execution can no longer proceed.
- **Aborted** :
	After the successful transaction has been rolled back and the database has been restored to its state prior to the start of transaction.
- **Committed** :
	After successful completion.

![[States of transaction.svg]]