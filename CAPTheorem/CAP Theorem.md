# CAP Theorem

In a  distributed computing environment  we can only support two of the following three characteristics:

- Consistency: Every read receives the most recent write or an error.
- Availability: Every request receives a response, without guarantee that it contains the most recent version of the information.
- Partition tolerance: The system continues to operate despite arbitrary partitioning due to network failures.

