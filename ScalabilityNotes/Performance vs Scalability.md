# Performance vs Scalability

## Difference between performance and scalability

A service is scalable if it results in increased performance in a manner proportional to resources added. Generally, increasing performance means serving more units of work, but it can also be to handle larger units of work, such as when dataset grow.

## A word on Scalability

- Why we would need to add more resource to a system ? Because we want to have redundancy.
- Scalability cannot be an after-thought, it has to be at the beginning of the system design stage.
- Another aspect of scalability is heterogeneity, this means that some nodes may not have a uniform performance, hence some algorithms relies on uniformity will either break down or do not efficiently utilize the resource.
- 