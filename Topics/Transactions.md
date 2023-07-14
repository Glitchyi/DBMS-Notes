A Transaction is a sequence of operations that must be executed as a whole
Basic operations are Read Write


## Concurrency Control
Several problems can occur when concurrent transactions execute in an
uncontrolled manner.
To avoid these problems concurrency control is needed.
Following are the types of problems we may encounter when transactions run
concurrently.
1. Lost update problem
2. Temporary update problem
3. Incorrect summary problem
4. Unrepeatable read problem


## Transaction States
1. BEGIN_TRANSACTION
▪ This marks the beginning of transaction execution.
2. READ or WRITE
▪ These specify read or write operations on database items that are executed
as part of a transaction.
3. END_TRANSACTION
▪ This specifies that READ and WRITE transaction operations have ended
and marks the end of transaction execution.
▪ At this point it may be necessary to check whether changes introduced by
the transaction can be permanently applied to the database (committed) or
whether the transaction has to be aborted because it violates serializability
or for some other reason.


## Conflict Equivalence
two schedules are said to be conflict equivalent if order of any two conflicting operations is same in both schedules.
• Conflict categories
1. Write-write conflict
2. Read-write conflict
3. Write-read conflict

## Testing for Conflict Serializability of a Schedule

Algorithm looks at only read_item and write_item operations in a schedule to construct a precedence graph (or serialization graph)

There is one node in graph for each transaction T i in schedule
Each edge ei in graph is of form (Tj→Tk), 1 ≤ j ≤ n,1 ≤ k ≤ n, where Tj is
starting node of ei and Tk is ending node of ei
Such an edge from node Tj to node Tk is created by algorithm if one of
operations in Tj appears in schedule before some conflicting operation in
Tk.

## CYCLE IN GRAPH BAD

