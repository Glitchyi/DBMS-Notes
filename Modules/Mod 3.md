## [[Topics/SQL|SQL]]

## VIEWS 
View are also called virtual tables, they are derived tables which rely upon existing tables for data and any change on the underlying tables will be reflected in the views.
View are used to summaries data or limit access to users and only see what is required

### Syntax
#syntax 
```SQL
CREATE VIEW <VIEW NAME> AS
SELECT <ATTRIBUTES>
FROM <TABLES>
WHERE <CONDITION>;
```
```SQL 
DROP VIEW <VIEW NAME>
```

### View Materialization
This involves the process of creating a temporary table which gets all the queries and is then updated to the view.
An efficient strategy for updating the view is when the database detects a change in tuples the view is re queried and the values are updated this is called the **concept of incremental update**.
If view has not been used in a while the computer removes the view and will recompute when required in the future

#### Updating of views is complicated and can be ambiguous
This is because for tables that may involve joins it will become an intricate process of properly updating the view.

## Assertions
They are conditions the database must always satisfy. Assertions are similar to CHECK but they are limited to a single table while the ASSERTIONS can be spanned across tables which make them more effective in maintaining the consistency of the entire database.

### Syntax 
#syntax
```SQL
CREATE ASSERTION <ASSERTION NAME>
CHECK <PREDICATE> 
/*The predicate can be any valid SQL expression or combination of expressions that evaluates to a Boolean value (true or false)*/
```
```SQL
DROP ASSERTION <ASSERTION NAME>
```

## Triggers
Triggers are stored procedures *(basically transaction event listener functions)*, Triggers can be used to perform any type of SQL querying given the transaction that triggered the event satisfies the provided conditions.

Benefits of Triggers
-  Generating some derived column values automatically
-  Enforcing referential integrity
-  Event logging and storing information on table access
-  Auditing
-  Synchronous replication of tables
-  Imposing security authorizations
-  Preventing invalid transactions

### Syntax
#syntax 
```SQL
CREATE [OR REPLACE] TRIGGER <TRIGGER NAME>
{ BEFORE | AFTER | INSTEAD OF }
{ INSERT | UPDATE | DELETE }
[OF <COLUMN NAME>]

ON <TABLES>
[REFERENCING OLD AS o NEW AS
[FOR EACH ROW]
 
WHEN (<CONDITION>)
 
DECLARE
	<Declration of statemetns like variables>
	
BEGIN
	Executable-statements
	
EXCEPTION
	Exception-handling-statements
END;
```

### Trigger Components
A tree constitutes of 3 components:
-  Event - When the trigger is activated
-  Condition - Conditional check to execute the trigger
-  Action - What the trigger does

### Eg. for a Trigger
```SQL 
CREATE OR REPLACE TRIGGER trigger_name
BEFORE DELETE OR INSERT OR UPDATE ON customers
FOR EACH ROW
WHEN (NEW.ID > 0)
DECLARE
  sal_diff NUMBER;
BEGIN
  sal_diff := :NEW.salary - :OLD.salary;
  
  dbms_output.put_line('Old salary: ' || :NEW.salary);
  dbms_output.put_line('New salary: ' || sal_diff);
  dbms_output.put_line('Salary difference: ' || sal_diff);
END;
```

#comparison

## Assertions vs Triggers

|Assertion|Trigger|
|-|-|
|Do Not Modify the data| More powerfull and can execute SQL statements|
|Are used for broader targeting| Used for very specific use cases|

## [[Topics/Physical Data Organization|Physical Data Organization]]

