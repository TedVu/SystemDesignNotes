# Availability Patterns

## Fail-over

### Active - passive

With active-passive, heartbeats are sent between the active and the passive server on standby, if the heartbeat is interrupted, the passive server takes over the active's IP address and resume service.

### Active - active

With active-active, both servers manage traffic spreading the load between them. If both servers are public-facing then DNS has to know about both servers, if both servers are internal servers then application logic server has to know about both servers.

## Replication

### Master - Slave replication

The master serves Reads and Writes request, then data is replicated from master to slave. If the master is offline the database operates in readonly mode until a new master is promoted.

![img](https://github.com/donnemartin/system-design-primer/raw/master/images/C9ioGtn.png)



### Master - master replication

Both masters can be read and write, if either master goes down the database can still operate in read and write mode.

![img](https://github.com/donnemartin/system-design-primer/raw/master/images/krAHLGg.png)
