[[Topics/Acid Compliancy|Acid Compliancy]]
[[Topics/Transactions]]
[[Topics/Schedules]]

## Concurrency Control Protocols
• The concurrency control protocols ensure the atomicity,
consistency, isolation, durability and serializability of the
concurrent execution of the database transactions.
• If every individual transaction follows concurrency control
protocol then all schedules in which those transaction
participate become serializable

## Lock Based Protocol
•Locking protocol means, whenever a transaction wants to perform any operation(Read/Write) on any data item, first it should request for lock on that data item.
• Once it acquire the lock then only it can perform the operation
•Locking mechanism is managed by Concurrency Control Subsystem

## Locks
- One way to ensure isolation of transactions is to require that data items be accessed in a mutually exclusive manner.
- That is, while one transaction is accessing a data item, no other transaction can modify that data item.
- Most common method used to implement this requirement is to allow a transaction to access a data item only if it is currently holding a lock on that item.
- Important locks that are used in concurrency control:
	• Binary Locks
	• Shared/Exclusive Locks

### Binary Locks
Two states locked and unlocked, check with LOCK(<>)

```
if LOCK(<>)==1                  TRANSACTION WAIT
if LOCK(<>)==0                 Set Lock to 1 and allowed to acces the items
```
### Shared Locks
```
read_lock(X)                      NO ONE CAN WRITE
write_lock(X)                     NO ONE CAN WRITE OR READ
unlock(X)                             TO UNLOCK
```

#Important 
## Two-Phase Locking(2PL) Protocol
One protocol that ensures serializability is two-phase locking protocol. This protocol requires that each transaction issue lock and unlock requests in two phases:
1. Growing or expanding phase (First phase): During this phase new locks on items can be acquired but none can be released.
2. Shrinking phase (Second phase): During this phase existing locks can be released but no new locks can be acquired.

Basically Growing phase get all locks, Shrinking phase lose all locks.

## Various 2PL
There are a number of variations of two-phase locking (2PL). Technique just described is known as basic 2PL. In practice, most popular variation of 2PL is strict 2PL, which guarantees strict schedules.

#### In strict 2PL, a transaction T does not release any of its exclusive(write) locks until after it commits or aborts. Strict 2PL is not deadlock-free.

#### A more restrictive variation of strict 2PL is rigorous 2PL, which also guarantees strict schedules.

#### Conservative 2PL (or static 2PL) requires a transaction to lock all items it accesses before transaction begins execution, by predeclaring its read-set and write-set.


## Dealing with Deadlock
- Deadlock occurs when each transaction T in a set of two or more transactions is waiting for some item that is locked by some other transaction T’ in set.


[[Topics/NoSQL]]
