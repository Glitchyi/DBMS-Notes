NoSQL database stands for “Not Only SQL” or “Not SQL.”

### Why NoSQL
NoSQL is scalable database that is flexible to store multiple formats of data in the same section, this makes it useful for data which is mixed in nature. 

## Features of NoSQL

### Non-relational
- NoSQL databases never follow the relational model
- Never provide tables with flat fixed-column records
- Work with self-contained aggregates or BLOBs
- Doesn’t require object-relational mapping and data normalization
- No complex features like query languages, query planners, referential integrity joins, ACID

### Schema-free
- NoSQL databases are either schema-free or have relaxed schemas
- Do not require any sort of definition of the schema of the data
- Offers heterogeneous structures of data in the same domain

###  Simple API
- Offers easy to use interfaces for storage and querying data provided
- APIs allow low-level data manipulation & selection methods
- Text-based protocols mostly used with HTTP REST with JSON
- Mostly used no standard based NoSQL query language
- Web-enabled databases running as internet-facing services

### Distributed
- Multiple NoSQL databases can be executed in a distributed fashion
- Offers auto-scaling and fail-over capabilities
- Often ACID concept can be sacrificed for scalability and throughput
- Mostly no synchronous replication between distributed nodes Asynchronous Multi- Master Replication, peer-to-peer, HDFS Replication
- Only providing eventual consistency

## Types of NoSQL Databases
- Key-Value Pair -  implements a hash table to store unique keys along with the pointers to the corresponding data values, 
  e.g. Redis

- Column oriented - While a relational database stores data in rows and reads data row by row, a column store is organized as a set of columns, 
```
So, let's say we have a table with information about people, and we want to store their names, ages, and addresses. In a row-oriented database, we would store one person's name, age, and address together as a row, and then the next person's information would be stored in the next row, and so on. But in a column-oriented database, we would store all the names together in one column, all the ages in another column, and all the addresses in a separate column
```
e.g. Casandra

- Graph based - Graph databases are generally straightforward in how they’re structured though. They primarily are composed of two components: node (data) & edge (relationship), 
  e.g. ArangoDB 

- Document oriented - Mongo ez
