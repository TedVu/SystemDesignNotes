# Scalability

## Part 1 - Clones

- Client will interact with our service via an Application Load Balancer.
- One users when interacting with the service do not have to know which server they are interacting with.
- One important aspect is that users have to have their session data persisted when interacting with your service.
- This leads to the first golden rule for scalability:
  - Every server contains exactly the same codebase and does not store any user-related data, like sessions or profile pictures, on local disc or memory.
- To ensure this, hence we can use a persistent cache such as Redis or Memcache, for deployment tools we can use some tools such as Capistrano to ensure all instances get the same code.



