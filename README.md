Google F1 is a distributed SQL database designed to support Google's AdWords business. It aims to provide the high availability and scalability typical of NoSQL systems like Bigtable while maintaining the consistency and usability of traditional SQL databases. Here are some key points about F1 based on the paper:

1. **Architecture**: F1 is built on Spanner, Google's globally distributed database, which offers synchronous cross-datacenter replication and strong consistency. F1 consists of stateless servers that interact with Spanner for data storage and processing. It includes components like clients, load balancers, F1 servers, and F1 master and slave nodes, with the F1 servers being mostly stateless except during transactions

2. **Data Model**: F1 uses a hierarchical schema where child tables are interleaved within parent tables, enhancing data locality and reducing query latency. This means that related data is physically stored together, optimizing read operations and reducing the need for complex joins across distributed servers.

3. **Transactions**: F1 supports multiple types of transactions, including snapshot, pessimistic, and optimistic transactions. By default, it uses optimistic transactions, which are beneficial for long-running, interactive user scenarios. This approach allows for efficient handling of transactions with fewer conflicts and improved system performance under high contention.

4. **Indexing**: F1 supports both local and global indexes, stored separately in Spanner. Local indexes are optimized for performance and data locality, while global indexes provide broader access but require more complex transaction handling. Developers are encouraged to use global indexes sparingly to maintain system efficiency.

5. **Schema Changes**: F1 allows for non-blocking schema changes, which are applied asynchronously across the distributed system. This ensures minimal disruption to ongoing operations and maintains data integrity by limiting schema versions in use at any given time to just two: the current and the next schema.

6. **Change History**: F1 includes robust support for change history, tracking changes in a detailed and structured manner. Each transaction generates change records, which are stored as child records within the database, allowing for efficient auditing and rollback operations.

In summary, F1 combines the best features of SQL and NoSQL databases, providing a scalable, highly available, and consistent platform that meets the demanding needs of Google's AdWords system. If you are interested in more technical details or specific use cases, I recommend reading the full paper on Google Research's publication site.



## References

[Warren’s notes](https://distributed-computing-musings.com/2023/10/paper-notes-f1-a-distributed-sql-database-that-scales/).

[Distributed Computing Musings](https://distributed-computing-musings.com/2023/10/paper-notes-f1-a-distributed-sql-database-that-scales/)