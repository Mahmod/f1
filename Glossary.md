### Glossary for Technical Terms Used in the Google F1 Paper

1. **Scalability**
   - **Definition**: The ability of a system to handle increased load by adding resources.
   - **Explanation**: In the context of F1, scalability means the system can grow to accommodate more data and users by adding more servers.

2. **Performance**
   - **Definition**: The speed and efficiency with which a system processes tasks.
   - **Explanation**: Performance refers to how quickly F1 can process queries and transactions, even under heavy load.

3. **Consistency**
   - **Definition**: Ensuring all users see the same data at the same time.
   - **Explanation**: In F1, consistency means that once data is written, all subsequent reads will return the same updated data.

4. **Transactions**
   - **Definition**: A sequence of database operations that are executed as a single unit.
   - **Explanation**: Transactions in F1 are used to ensure that multiple operations either all succeed or all fail, maintaining data integrity.

5. **SQL (Structured Query Language)**
   - **Definition**: A standard language for managing and manipulating databases.
   - **Explanation**: F1 uses SQL to allow developers to query and update the database using familiar syntax.

6. **NoSQL**
   - **Definition**: A type of database that can handle large volumes of data and is designed for scalability.
   - **Explanation**: NoSQL databases, like Bigtable, are used in F1 to provide scalability and performance.

7. **Spanner**
   - **Definition**: Google's globally distributed database that provides the underlying infrastructure for F1.
   - **Explanation**: Spanner handles data replication and storage across multiple data centers, ensuring high availability and strong consistency.

8. **Load Balancers**
   - **Definition**: Devices or software that distribute network or application traffic across multiple servers.
   - **Explanation**: In F1, load balancers help distribute the workload evenly across servers to optimize performance and avoid overloading any single server.

9. **ORM (Object-Relational Mapping)**
   - **Definition**: A programming technique for converting data between incompatible systems using object-oriented programming languages.
   - **Explanation**: F1 includes an ORM library to help developers interact with the database using objects rather than raw SQL queries.

10. **Hierarchical Schema**
    - **Definition**: A data model where data is organized in a tree-like structure.
    - **Explanation**: F1 uses a hierarchical schema to store related data close together, improving query performance.

11. **Two-Phase Commit (2PC)**
    - **Definition**: A protocol used to ensure all participants in a distributed transaction agree on the outcome.
    - **Explanation**: 2PC in F1 ensures that distributed transactions are completed correctly, even when involving multiple servers.

12. **Pessimistic Transactions**
    - **Definition**: Transactions that lock resources during the read phase to prevent conflicts.
    - **Explanation**: F1 uses pessimistic transactions to avoid conflicts by locking data during the entire transaction.

13. **Optimistic Transactions**
    - **Definition**: Transactions that do not lock resources during the read phase but check for conflicts before committing.
    - **Explanation**: F1's default transaction type, which improves performance by allowing multiple transactions to proceed concurrently, checking for conflicts only at the end.

14. **Snapshot Transactions**
    - **Definition**: Read-only transactions that capture the state of the data at a specific point in time.
    - **Explanation**: Snapshot transactions in F1 provide a consistent view of the data as it existed at a particular moment, without locking the data.

15. **Protocol Buffers**
    - **Definition**: A method developed by Google for serializing structured data.
    - **Explanation**: F1 uses protocol buffers to efficiently store and retrieve complex data structures within the database.

16. **Indexing**
    - **Definition**: A database optimization technique that improves the speed of data retrieval operations.
    - **Explanation**: F1 uses local and global indexes to quickly locate data without scanning the entire database.

17. **Local Index**
    - **Definition**: An index that is stored with the data it references, providing fast access within a specific part of the database.
    - **Explanation**: In F1, local indexes are used to optimize queries within a localized portion of the data.

18. **Global Index**
    - **Definition**: An index that spans across the entire database, providing a way to quickly access data spread over multiple servers.
    - **Explanation**: F1 uses global indexes for broader queries, though they involve more complex transaction handling.

19. **Schema Changes**
    - **Definition**: Modifications to the structure of the database (e.g., adding or removing tables or columns).
    - **Explanation**: F1 allows schema changes to happen without downtime, ensuring continuous operation and data integrity.

20. **Change History**
    - **Definition**: A record of all changes made to the database.
    - **Explanation**: F1 tracks changes at a detailed level, allowing for easy auditing and rollback if needed.

21. **Latency**
    - **Definition**: The delay before a transfer of data begins following an instruction for its transfer.
    - **Explanation**: In F1, low latency means queries are processed quickly, even with large amounts of data.


22. **Availability**
    - **Definition**: The degree to which a system is operational and accessible when required for use.
    - **Explanation**: F1 ensures high availability, meaning it is designed to be up and running nearly all the time, even in the face of failures.

23. **Data Locality**
    - **Definition**: The practice of storing data close to where it is used.
    - **Explanation**: F1 clusters related data together to reduce the time it takes to access that data, improving performance and efficiency.

24. **Distributed Systems**
    - **Definition**: Systems in which components located on networked computers communicate and coordinate their actions by passing messages.
    - **Explanation**: F1 is a distributed system, meaning it runs on many servers that work together to handle data and queries.

25. **Synchronous Replication**
    - **Definition**: The process of copying data to multiple locations simultaneously.
    - **Explanation**: F1 uses synchronous replication to ensure that data is copied across data centers at the same time, maintaining consistency.

26. **Asynchronous Schema Change**
    - **Definition**: Schema changes that occur without immediately applying the changes to all parts of the database at once.
    - **Explanation**: In F1, schema changes happen in phases to ensure the database remains operational during updates.

27. **Stateless Server**
    - **Definition**: A server that does not retain information about client sessions between requests.
    - **Explanation**: F1 servers are mostly stateless, meaning they do not keep data about transactions once they are complete, which helps with scalability.

28. **MapReduce**
    - **Definition**: A programming model for processing large data sets with a distributed algorithm.
    - **Explanation**: F1 uses MapReduce jobs for tasks like updating the schema across the database.

29. **Lease**
    - **Definition**: A time-limited contract granting temporary access to a resource.
    - **Explanation**: F1 servers acquire leases to use certain schemas during updates, ensuring consistency and preventing conflicts.

30. **Two-Phase Locking (2PL)**
    - **Definition**: A concurrency control method that ensures serializability in transactions.
    - **Explanation**: Spanner, and thus F1, uses two-phase locking to manage access to data during transactions, preventing conflicts and ensuring data integrity.

31. **Publish-Subscribe Model**
    - **Definition**: A messaging pattern where senders (publishers) send messages to channels, and receivers (subscribers) get messages from these channels.
    - **Explanation**: F1 uses a publish-subscribe system to notify other parts of the system about data changes, facilitating timely updates and actions.

32. **Blob (Binary Large Object)**
    - **Definition**: A collection of binary data stored as a single entity in a database.
    - **Explanation**: In F1, protocol buffers are stored as blobs, allowing complex data structures to be handled efficiently.

33. **Concurrency Control**
    - **Definition**: Techniques used to ensure that database transactions are performed concurrently without violating data integrity.
    - **Explanation**: F1 uses mechanisms like two-phase locking and optimistic transactions to manage concurrency, ensuring multiple users can interact with the database without conflicts.

34. **Data Replication**
    - **Definition**: The process of copying data from one location to another to ensure consistency and reliability.
    - **Explanation**: F1 replicates data across multiple servers and data centers to ensure high availability and fault tolerance.

35. **Fault Tolerance**
    - **Definition**: The ability of a system to continue operating properly in the event of the failure of some of its components.
    - **Explanation**: F1 is designed to be fault-tolerant, meaning it can handle server failures without losing data or disrupting service.

36. **Distributed Query Execution**
    - **Definition**: The process of executing a database query across multiple servers.
    - **Explanation**: In F1, queries are distributed across many servers to balance the load and speed up processing.

37. **Latency p50/p99**
    - **Definition**: Metrics for measuring latency, where p50 is the median (50th percentile) and p99 is the 99th percentile.
    - **Explanation**: These metrics help understand the typical and worst-case response times in F1, showing how quickly most queries are processed and the outliers that take longer.

38. **Root Table**
    - **Definition**: The primary table in a hierarchical database schema.
    - **Explanation**: In F1, root tables hold the main entities, with related data in child tables linked by foreign keys.

39. **Child Table**
    - **Definition**: A table that is hierarchically related to a root table, storing related data.
    - **Explanation**: Child tables in F1 have their primary keys prefixed with the parent table's primary key, ensuring data is stored in a related and efficient manner.

40. **Two-Phase Locking (2PL)**
    - **Definition**: A concurrency control method that involves acquiring locks during the first phase and releasing them during the second phase.
    - **Explanation**: F1 uses 2PL to ensure that all changes in a transaction are made atomically, avoiding conflicts and ensuring consistency.

41. **Protocol Buffers**
    - **Definition**: A method developed by Google for serializing structured data.
    - **Explanation**: Protocol buffers are used in F1 to efficiently store and transmit complex data structures.

42. **Schema Repository**
    - **Definition**: A centralized location where database schema information is stored.
    - **Explanation**: F1 uses a schema repository to manage and apply schema changes across its distributed system.

43. **High Availability**
    - **Definition**: A system design approach that ensures a high level of operational performance, often through redundancy.
    - **Explanation**: F1 is designed for high availability, meaning it remains accessible and operational almost all the time, even during failures.

44. **Fault Tolerance**
    - **Definition**: The capability of a system to continue functioning correctly even when some of its components fail.
    - **Explanation**: F1’s architecture includes mechanisms to detect and recover from faults without impacting overall system performance.

45. **Sharding**
    - **Definition**: A database partitioning technique to distribute data across multiple machines.
    - **Explanation**: F1 uses sharding to divide large datasets into smaller, more manageable pieces that can be spread across different servers.

46. **Load Balancer**
    - **Definition**: A device or software that distributes network or application traffic across multiple servers.
    - **Explanation**: Load balancers in F1 help manage incoming queries by distributing the load evenly across servers to ensure no single server is overwhelmed.

47. **Operational Simplicity**
    - **Definition**: The ease with which a system can be managed and maintained.
    - **Explanation**: Despite its complexity, F1 aims to provide operational simplicity by automating many routine tasks associated with database management.

48. **Latency**
    - **Definition**: The delay between a request for data and the delivery of the data.
    - **Explanation**: F1 strives to minimize latency to ensure fast response times for queries.

49. **Distributed Transactions**
    - **Definition**: Transactions that span multiple databases or servers.
    - **Explanation**: F1 supports distributed transactions to maintain consistency across different parts of the database, even when data is spread over multiple servers.

50. **Data Partitioning**
    - **Definition**: The division of a database into distinct, independent segments.
    - **Explanation**: F1 uses data partitioning to improve performance and manageability by dividing large tables into smaller, more manageable pieces.

51. **Replication**
    - **Definition**: The process of copying data from one location to another to ensure consistency and availability.
    - **Explanation**: F1 uses replication to keep data synchronized across multiple servers, ensuring it remains available even if some servers fail.

52. **Concurrency**
    - **Definition**: The ability of a system to handle multiple operations or transactions simultaneously.
    - **Explanation**: F1 employs various concurrency control mechanisms to manage multiple transactions at the same time without conflicts.

53. **Replication Lag**
    - **Definition**: The delay between the time data is written to the primary server and when it is replicated to secondary servers.
    - **Explanation**: F1 aims to minimize replication lag to ensure data consistency and availability across all servers.

54. **Consistency Models**
    - **Definition**: The rules and guarantees provided by a database system about the visibility and order of updates.
    - **Explanation**: F1 uses strong consistency models to ensure that all users see the same data at the same time, regardless of which server they are connected to.

55. **Throughput**
    - **Definition**: The number of transactions or operations a system can process in a given period.
    - **Explanation**: F1 is designed to maximize throughput, handling a large number of transactions per second to support high-demand applications.

56. **Horizontal Scaling**
    - **Definition**: Adding more machines or nodes to a system to increase its capacity.
    - **Explanation**: F1 uses horizontal scaling to grow its capacity by simply adding more servers, making it easier to handle more data and users.

57. **Vertical Scaling**
    - **Definition**: Increasing the capacity of a single machine or node, typically by adding more resources like CPU or memory.
    - **Explanation**: While F1 primarily relies on horizontal scaling, it can also benefit from vertical scaling to improve the performance of individual servers.

58. **Data Center**
    - **Definition**: A facility used to house computer systems and associated components, such as telecommunications and storage systems.
    - **Explanation**: F1 operates across multiple data centers, ensuring high availability and disaster recovery capabilities.

59. **Cross-Datacenter Replication**
    - **Definition**: The process of copying data between different data centers to ensure data availability and durability.
    - **Explanation**: F1 uses cross-datacenter replication to ensure that data remains accessible even if one data center experiences a failure.

60. **Schema Evolution**
    - **Definition**: The process of changing the schema of a database over time to accommodate new requirements.
    - **Explanation**: F1 supports schema evolution, allowing changes to the database structure without significant downtime.

61. **Asynchronous Operations**
    - **Definition**: Operations that occur independently of the main program flow, allowing other processes to run simultaneously.
    - **Explanation**: In F1, asynchronous operations allow tasks like schema changes and data replication to happen without blocking other operations, improving overall system efficiency.

62. **Data Locality**
    - **Definition**: The practice of storing related data close together to minimize access time.
    - **Explanation**: F1 ensures data locality by storing related records (like a customer and their orders) in close proximity, reducing the time it takes to retrieve related data.

63. **Hierarchical Storage**
    - **Definition**: A storage structure where data is organized in a tree-like format with parent and child relationships.
    - **Explanation**: F1 uses hierarchical storage to keep related data together, which helps in efficiently processing queries involving multiple related tables.

64. **Lock Management**
    - **Definition**: The system that controls access to data by managing locks to prevent concurrent access issues.
    - **Explanation**: F1 employs sophisticated lock management techniques to ensure that data remains consistent and free of conflicts during concurrent transactions.

65. **Data Integrity**
    - **Definition**: The accuracy and consistency of data over its lifecycle.
    - **Explanation**: F1 maintains data integrity through transactions and strong consistency models, ensuring that the data remains accurate and reliable.

66. **Partitioning**
    - **Definition**: Dividing a database into smaller, more manageable pieces.
    - **Explanation**: F1 uses partitioning to distribute data across multiple servers, which helps in managing large datasets and improving query performance.

67. **Fault Detection**
    - **Definition**: The process of identifying and diagnosing system failures.
    - **Explanation**: F1 includes mechanisms for detecting faults in the system and taking corrective actions to maintain high availability and reliability.

68. **Protocol Buffers**
    - **Definition**: A language-neutral, platform-neutral extensible mechanism for serializing structured data.
    - **Explanation**: Protocol buffers are used in F1 to efficiently serialize and deserialize data, making it easier to store and transmit complex data structures.

69. **Query Optimization**
    - **Definition**: Techniques used to improve the efficiency of database queries.
    - **Explanation**: In F1, query optimization involves choosing the best execution plan to retrieve data quickly, minimizing response time and resource usage.

70. **Execution Plan**
    - **Definition**: The strategy used by the database to execute a query.
    - **Explanation**: An execution plan in F1 details the steps the system will take to execute a SQL query, including how to access data and perform joins.

71. **Distributed Query Execution**
    - **Definition**: The process of executing queries across multiple servers or nodes in a distributed database.
    - **Explanation**: F1 executes queries across many servers to balance the load and improve performance, leveraging the distributed nature of its architecture.

72. **Paxos**
    - **Definition**: A consensus algorithm used to achieve agreement on a single value among distributed systems.
    - **Explanation**: Spanner, which underlies F1, uses Paxos to ensure data consistency and agreement across its distributed nodes.

73. **Replica**
    - **Definition**: A copy of a database or dataset stored in a different location.
    - **Explanation**: F1 maintains replicas of data across multiple servers and data centers to ensure high availability and fault tolerance.

74. **Data Sharding**
    - **Definition**: Dividing a large database into smaller, more manageable pieces called shards.
    - **Explanation**: F1 uses sharding to distribute data across multiple servers, which helps in managing large volumes of data and improving query performance.

75. **Failover**
    - **Definition**: The process of switching to a backup system when the primary system fails.
    - **Explanation**: F1 supports failover mechanisms to ensure continuous availability, automatically redirecting traffic to backup servers if a primary server fails.