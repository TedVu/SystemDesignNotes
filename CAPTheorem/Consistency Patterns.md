# Consistency Patterns

## Weak consistency

After a write, read may or may not see it. A best effort approach is taken.

The systems demonstrate this approach are VoIP, video chat and realtime multiplayer game.

## Eventual consistency

After a write, read will eventually see it, data is replicated asynchronously.

The system demonstrate this approach are DNS and email.

## Strong consistency

After a write, reads will see it, data is replicated synchronously.

The system demonstrates this approach are file system and RDBMs.

