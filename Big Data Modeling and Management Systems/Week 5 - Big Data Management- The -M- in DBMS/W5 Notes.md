# Why Data Management? #

high volume data and two contrasting approaches for handling them. 


## Problems with File Management Systems ##
- First, there are multiple file formats. And often, there was a duplication of information in different files. Or the files simply had inconsistent information that was very hard to determine, especially when the data was large and the file content was complex. 
- Secondly, there wasn't a uniform way to access data. Each data access task needed to be written as a separate program. So people ended up writing different programs for data access, as well as data update. 
- A third problem was rooted to the enforcement of constraints, often called integrity constraints. So if you want to change the constraint, you need to look for the programs where such a rule is hard coded. 
- The fourth problem has to do with system failures.
## Advantages. of DBMS ## 
- Declarative query Language.
DBMSs offer query languages, which are declarative. Declarative means that we state what we want to retrieve without telling the DBMS how exactly to retrieve it. 
- Data Independence. 
A typical user of a DBMS who issues queries does not worry about how the relations are structured or whether they are located in the same machine, or spread across five machines.
- Efficient Access through Optimization
Relational DBMSs have developed a very mature and continually improving methodology of how to answer a query efficiently, even when there are a large number of cables and the number of records exceeds hundreds of millions. 

## Parallel and Distributed DBMS ##
DBMSs have handled the issue of large volumes is by created parallel and distributed databases.
**Parallel Database System**
In a parallel database, for example, parallel Oracle, parallel DB2 or post SQL XE. The tables are spread across multiple machines and operations like selection, and join use parallel algorithms to be more efficient. These systems also allow a user to create a replication. That is multiple copies of tables. Thus, introducing data redundancy, so that failure on replica can be compensated for by using another. Further, it replicates in sync with each other and a query can result into any of the replicates. This increases the number of simultaneous that is conquer into queries that can be handled by the system. 

**Distributed Database System**
A distributed DBMS, which we'll not discuss in detail in this course is a network of independently running DBMSs that communicate with each other. In this case, one component knows some part of the schema of it is neighboring DBMS and can pass a query or part of a query to the neighbor when needed. 

# From DBMS to BDMS #
## Desired Characteristics of BDMS ##
- Flexible, Semistructured data model
- Support different data types
- A full query language
- Efficient parallel query runtime
- Wide range of query size
- Continious data ingestion (Streaming Data)
- Scale gracefully to manage and query large volumes of Data
- Full Data Management capability

## BASE Properties ##
- BA: Basic Availability: This states that the system does guarantee the availability of data in the following sense. If you make a request, there will be a response to that request. 
- S: Soft state: Which means the state of the system is very likely to change over time. So even during times without input, there may be changes going on through the system due to eventual consistency. 
- E: Eventual Consistency: This means that the system will eventually become consistent once it stops receiving input. 

## CAP Theorem ## 
Also named Bauer's theorem after the computer scientist Eric Bauer. He states, that it is impossible for a distributed computer system to simultaneously provide all three of the following guarantees. Consistency. It means all nodes say they same data at any time. Availability, which is a guarantee that every request receives a response about whether it succeeded or failed. And Partition Tolerance, which means the system continues to operate despite arbitrary partitioning due to network failures. 
