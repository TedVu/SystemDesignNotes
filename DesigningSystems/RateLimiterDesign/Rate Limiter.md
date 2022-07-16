# Rate Limiter



## Step 1 - Understand the problem and establish design scope

**Question 1**: What's a Rate Limiter ? 

A rate limiter is a service that can limit the request for another service, rate limiter is usually associated with APIs. The benefits of the rate limiter are:

- Avoid DDos
- Prevent service overload.
- Better allocate and control resource.

**Question 2**: Does the rate limiter throttle API requests based on IP, the user ID, or other properties.

Rate limiter should be flexible enough to throttle API requests based on different condition.

Final requirement based on analysis:

- Accurately limit excessive requests.
- Low latency.
- Use as little memory as possible.
- Worked in distributed environment.
- High fault tolerance.
- Have good exception handling.

Two types of requirements

- General requirements
- Technical requirements related to Rate Limiter.

## Step 2 - Propose a high level design

### Question 1:  Where to put the rate limiter ? 

There are 3 potential areas that we can place a rate limiter at:

- Client side
- Server side
- Middleware (this is what will be discussed in detail)

### Question 2: What algorithms should be used to implement the rate limiter ?

Some popular rate limiting algorithms include:

- Token bucket
- Leaking bucket
- Sliding window counter
- Fixed window counter
- Sliding window log

Each algorithms has its own strength and weaknesses and choosing the most suitable algorithm relies on many factors.

## Step 3 - Design deep dive

See more on the detailed design diagram, overall we should consider these following factors:

- How are rate limiting rules stored and retrieved ? 
- How should we handle overflow request ?
- Where should we include the response to user to show that the call is successful or failed ?
- Discuss operation of the design in a distributed environment, how to handle synchronization and race condition problem.
- Discuss performance.
- Discuss monitoring technique.

## Step 4 - Wrap up

We can discuss many other factors such as:

- What level of rate limiting are we implementing ? We only focus on implementing rate limiting at level 7 (Application layer).
- 
