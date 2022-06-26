# CAP Theorem

In a  distributed computing environment  we can only support two of the following three characteristics:

- Consistency: Every read receives the most recent write or an error.
- Availability: Every request receives a response, without guarantee that it contains the most recent version of the information.
- Partition tolerance: The system continues to operate despite arbitrary partitioning due to network failures.

Note that we need to always support partition tolerance as networks aren't reliable, hence we must choose between these two:

CP - consistency and partition tolerance

We implement in such a way that waiting for a response from a partitioned node might result in a timeout error.

Banking software usually supports this characteristics.

AP - availability and partition tolerance

Responses returns the most readily available version of the data available on any node, in this case we support other type of consistency known as eventual consistency.

