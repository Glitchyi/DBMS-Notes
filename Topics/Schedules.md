## Recoverable Schedule
• A schedule is recoverable if each transaction commits only after all the transactions from which it has read has committed.

#Important 
If a transaction Tj reads a data item written by transaction Ti, then the commit
operation of Tj should happen only after the commit Ti, then such schedules
are recoverable.
If a transaction Tj reads a data item written by transaction Ti and commit
operation of Tj is before the commit of Ti, then such schedules are
irrecoverable.

### Recoverable schedules are further categorized into 3 types:
1.Cascading Schedule
2.Cascadeless Schedule
3.Strict Schedule

## Cascading Schedule
• Because of a single failure in a particular transaction, if all dependent transactions need to be rolled back, it is called as Cascading Schedule/Cascading Rollbacks/ Cascading Abort.
• Such schedules are recoverable, but can be time consuming since numerous transactions can be rolled back.
• Complete waste of work, time and resources.
• To avoid cascading rollbacks, we need Cascade less schedules.

## Cascade less Schedules
• Schedule which are free from Cascading Rollbacks
• If every transaction in the schedule reads only items that were written by a committed transaction, then such a schedule is called Cascade less schedule.

## Strict Schedule
• More restrictive type of schedule.
• In a schedule, a transaction is neither allowed to read/write a data item until the transaction that has write is committed or aborted.

## Non-recoverable Schedule
• If a transaction reads the value of an operation from an
uncommitted transaction and commits before the transaction
from where it has read the value, then such a schedule is
called Non-Recoverable schedule.
•A non recoverable schedule means when there is a system
failure, we may not be able to recover to a consistent database
state.