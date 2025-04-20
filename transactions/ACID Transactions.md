tags : #transactions

#### Introduction : 

ACID transaction are set rules that should be followed by any data extensive application to ensure that data stored in database is accurate and reliable. On the most abstract level ACID transactions can be explained as, 

- Atomicity : 
	Atomicity is a principle to ensure that any transaction should completely committed or aborted instantly in case of any error. This is also know as 'all or nothing' approach as it states either entire transaction will be committed or no change will be committed at all.
- Consistency : 
	Consistency is a principle that ensures all the data committed in transaction follows the rules and regulation imposed on the relation. Data before start of transaction and after completion of transaction should be according to constraints that are imposed on the relation.
- Isolation : 
	Isolation is a principle which states the each transaction should be isolated, that is, it should not be relied upon other transactions for its completion. Isolation property states that each transaction is completed independently. This property prevent issues like dirty reads, lost updates and inconsistent data.
- Durability : 
	Durability principle states that after the data is committed it should be available in database forever and should not be lost due to errors such as power shortage, hardware failure or hardware malfunctions etc. 