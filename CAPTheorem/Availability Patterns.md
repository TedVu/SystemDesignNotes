# Availability Patterns

## Fail-over

### Active - passive

With active-passive, heartbeats are sent between the active and the passive server on standby, if the heartbeat is interrupted, the passive server takes over the active's IP address and resume service.

### Active - active

With active-active, both servers manage traffic spreading the load between them. If both servers are public-facing then DNS has to know about both servers, if both servers are internal servers then application logic server has to know about both servers.

