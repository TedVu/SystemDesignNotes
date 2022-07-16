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

