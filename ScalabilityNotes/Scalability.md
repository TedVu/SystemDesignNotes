# Scalability

## Part 1 - Clones

- Client will interact with our service via an Application Load Balancer.
- One users when interacting with the service do not have to know which server they are interacting with.
- One important aspect is that users have to have their session data persisted when interacting with your service.
- This leads to the first golden rule for scalability:
  - Every server contains exactly the same codebase and does not store any user-related data, like sessions or profile pictures, on local disc or memory.
- To ensure this, hence we can use a persistent cache such as Redis or Memcache, for deployment tools we can use some tools such as Capistrano to ensure all instances get the same code.

## Part 2 - Database

- MySQL is a logical and safe choice to start off with but soon the performance will degrade, at this stage there are two major paths which can be taken:
  - Scale vertically and use relational database techniques, to scale vertically we can add more RAMs. Other relational database techniques which can help improve the performance of database are: SQL tuning, denormalization, sharding. We can also utilize some techniques such as replication with master-slave replication.
  - Scale horizontally by switching to NoSQL database such as MongoDB or CouchDB.

## Part 3  - Cache

- Cache is a buffer that sits between the application and data storage.
- Cache holds all the dataset in-memory with RAMs, hence the speed is lightning-fast.
- There are two major in-memory cache databases: Memcache and Redis.
- Memcache provides good scalability.
- Redis supports data persitence and provides many Data structure such as set or list.
- Next we consider some of the caching patterns:
  - Cache queries: This is the commonly used, but it has some advantages such as when a datacell changes we have to delete all queries which have that data cell.
  - Cache object: Store the object in the cache.
- Some ideas of objects to cache:
  - user sessions (never use the database !).
  - fully rendered blog articles.
  - activity streams.
  - user <-> friend relationships.